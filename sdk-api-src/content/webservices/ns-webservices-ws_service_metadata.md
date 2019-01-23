---
UID: NS:webservices._WS_SERVICE_METADATA
title: WS_SERVICE_METADATA
author: windows-sdk-content
description: Specifies the service metadata documents array. This can be a collection of WSDL/XSD documents represented as an array of WS_STRING.
old-location: wsw\ws_service_metadata.htm
tech.root: wsw
ms.assetid: f695867d-989d-41a9-ab6e-612a6ef4fb14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_SERVICE_METADATA, WS_SERVICE_METADATA structure [Web Services for Windows], webservices/WS_SERVICE_METADATA, wsw.ws_service_metadata
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_METADATA
product: Windows
targetos: Windows
req.typenames: WS_SERVICE_METADATA
req.redist: 
---

# WS_SERVICE_METADATA structure


## -description


Specifies the service metadata documents array. This can be a collection of 
                WSDL/XSD documents represented as an array of WS_STRING.
            


## -struct-fields




### -field documentCount

The count of metadata documents being specified.
                


### -field documents

A <a href="https://msdn.microsoft.com/en-us/library/Dd323427(v=VS.85).aspx">WS_SERVICE_METADATA_DOCUMENT</a>* array where element represents a WS_SERVICE_METADATA_DOCUMENT for each individual XML Schema, WSDL or a Policy document. 
                The service model expects this to be valid for the lifetime of the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>. 
            


### -field serviceName

Reference to WS_XML_STRING representing the name of the service in the WSDL document. Note that this field must be specified along with the serviceNs field. The service model expects this to be valid for the lifetime 
                    of the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>.
                


### -field serviceNs

Reference to WS_XML_STRING representing the namespace of the service in the WSDL document. Note that this field must be specified along with the serviceName field.
                The service model expects this to be valid for the lifetime of the <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a>.
            

