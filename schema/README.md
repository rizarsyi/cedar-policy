{
    "myStore": {
        "commonTypes": {
            "email_address": {
                "type": "Record",
                "attributes": {
                    "domain": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "uid": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    }
                }
            },
            "Url": {
                "type": "Record",
                "attributes": {
                    "host": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "path": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "protocol": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    }
                }
            },
            "Context": {
                "type": "Record",
                "attributes": {
                    "current_time": {
                        "type": "EntityOrCommon",
                        "name": "Long"
                    },
                    "device_health": {
                        "type": "Set",
                        "element": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        }
                    },
                    "fraud_indicators": {
                        "type": "Set",
                        "element": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        }
                    },
                    "geolocation": {
                        "type": "Set",
                        "element": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        }
                    },
                    "network": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "network_type": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "operating_system": {
                        "type": "EntityOrCommon",
                        "name": "String"
                    },
                    "user_agent": {
                        "type": "EntityOrCommon",
                        "required": false,
                        "name": "String"
                    }
                }
            }
        },
        "entityTypes": {
            "Access_token": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "aud": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "exp": {
                            "type": "EntityOrCommon",
                            "name": "Long"
                        },
                        "iat": {
                            "type": "EntityOrCommon",
                            "name": "Long"
                        },
                        "iss": {
                            "type": "EntityOrCommon",
                            "name": "TrustedIssuer"
                        },
                        "jti": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "nbf": {
                            "type": "EntityOrCommon",
                            "name": "Long"
                        },
                        "scope": {
                            "type": "Set",
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        }
                    }
                }
            },
            "Application": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "app_id": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "name": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "url": {
                            "type": "EntityOrCommon",
                            "name": "Url"
                        }
                    }
                }
            },
            "HTTP_Request": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "accept": {
                            "type": "Set",
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "header": {
                            "type": "Set",
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "url": {
                            "type": "EntityOrCommon",
                            "name": "Url"
                        }
                    }
                }
            },
            "id_token": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "acr": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "amr": {
                            "type": "Set",
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "aud": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "azp": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "birthdate": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "email": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "email_address"
                        },
                        "exp": {
                            "type": "EntityOrCommon",
                            "name": "Long"
                        },
                        "iat": {
                            "type": "EntityOrCommon",
                            "name": "Long"
                        },
                        "iss": {
                            "type": "EntityOrCommon",
                            "name": "TrustedIssuer"
                        },
                        "jti": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "name": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "phone_number": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "role": {
                            "type": "Set",
                            "required": false,
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "sub": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        }
                    }
                }
            },
            "Role": {},
            "TrustedIssuer": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "issuer_entity_id": {
                            "type": "EntityOrCommon",
                            "name": "Url"
                        }
                    }
                }
            },
            "User": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "email": {
                            "type": "EntityOrCommon",
                            "name": "email_address"
                        },
                        "phone_number": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "role": {
                            "type": "Set",
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "sub": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "username": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        }
                    }
                },
                "memberOfTypes": [
                    "Role"
                ]
            },
            "Userinfo_token": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "aud": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "birthdate": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "email": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "email_address"
                        },
                        "exp": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "Long"
                        },
                        "iat": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "Long"
                        },
                        "iss": {
                            "type": "EntityOrCommon",
                            "name": "TrustedIssuer"
                        },
                        "jti": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "name": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "phone_number": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "role": {
                            "type": "Set",
                            "required": false,
                            "element": {
                                "type": "EntityOrCommon",
                                "name": "String"
                            }
                        },
                        "sub": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        }
                    }
                }
            },
            "Workload": {
                "shape": {
                    "type": "Record",
                    "attributes": {
                        "client_id": {
                            "type": "EntityOrCommon",
                            "name": "String"
                        },
                        "iss": {
                            "type": "EntityOrCommon",
                            "name": "TrustedIssuer"
                        },
                        "name": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "rp_id": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        },
                        "spiffe_id": {
                            "type": "EntityOrCommon",
                            "required": false,
                            "name": "String"
                        }
                    }
                }
            }
        },
        "actions": {
            "Compare": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "DELETE": {
                "appliesTo": {
                    "principalTypes": [
                        "Workload"
                    ],
                    "resourceTypes": [
                        "HTTP_Request"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Execute": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "GET": {
                "appliesTo": {
                    "principalTypes": [
                        "Workload"
                    ],
                    "resourceTypes": [
                        "HTTP_Request"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "HEAD": {
                "appliesTo": {
                    "principalTypes": [
                        "Workload"
                    ],
                    "resourceTypes": [
                        "HTTP_Request"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Monitor": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "PATCH": {
                "appliesTo": {
                    "principalTypes": [
                        "Workload"
                    ],
                    "resourceTypes": [
                        "HTTP_Request"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "PUT": {
                "appliesTo": {
                    "principalTypes": [
                        "Workload"
                    ],
                    "resourceTypes": [
                        "HTTP_Request"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Read": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Search": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Share": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Tag": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            },
            "Write": {
                "appliesTo": {
                    "principalTypes": [
                        "User",
                        "Role",
                        "Workload"
                    ],
                    "resourceTypes": [
                        "Application"
                    ],
                    "context": {
                        "type": "Context"
                    }
                }
            }
        }
    }
}