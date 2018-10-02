---
UID: NE:webservices.WS_METADATA_PROPERTY_ID
title: WS_METADATA_PROPERTY_ID
author: windows-sdk-content
description: Each metadata property is of type WS_METADATA_PROPERTY, is identified by an ID, and has an associated value. If a property is not specified when the metadata is created, then its default value is used.
old-location: wsw\ws_metadata_property_id.htm
tech.root: wsw
ms.assetid: d3baa961-4701-4f2f-9263-5ac0266f6056
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_METADATA_PROPERTY_HEAP_PROPERTIES, WS_METADATA_PROPERTY_HEAP_REQUESTED_SIZE, WS_METADATA_PROPERTY_HOST_NAMES, WS_METADATA_PROPERTY_ID, WS_METADATA_PROPERTY_ID enumeration [Web Services for Windows], WS_METADATA_PROPERTY_MAX_DOCUMENTS, WS_METADATA_PROPERTY_POLICY_PROPERTIES, WS_METADATA_PROPERTY_STATE, WS_METADATA_PROPERTY_VERIFY_HOST_NAMES, webservices/WS_METADATA_PROPERTY_HEAP_PROPERTIES, webservices/WS_METADATA_PROPERTY_HEAP_REQUESTED_SIZE, webservices/WS_METADATA_PROPERTY_HOST_NAMES, webservices/WS_METADATA_PROPERTY_ID, webservices/WS_METADATA_PROPERTY_MAX_DOCUMENTS, webservices/WS_METADATA_PROPERTY_POLICY_PROPERTIES, webservices/WS_METADATA_PROPERTY_STATE, webservices/WS_METADATA_PROPERTY_VERIFY_HOST_NAMES, wsw.ws_metadata_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WS_METADATA_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: WS_METADATA_PROPERTY_ID
req.redist: 
---

# WS_METADATA_PROPERTY_ID enumeration


## -description


Each metadata property is of type <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a>, is identified by an ID, and has an associated value.  If a property is not specified when the metadata is created,
                then its default value is used.
            


## -enum-fields




### -field WS_METADATA_PROPERTY_STATE

This property is used with <a href="https://msdn.microsoft.com/21d8dbca-e8a5-4b2f-a1f7-951532922024">WsGetMetadataProperty</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> structure contains  the current <a href="https://msdn.microsoft.com/4d2b8c31-d5ff-4b96-9aaf-57e59d075431">WS_METADATA_STATE</a> of the metadata object.
                


### -field WS_METADATA_PROPERTY_HEAP_PROPERTIES

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> to specify
                    properties of the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> object used by the metadata
                    object to store information about the metadata that was read.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> structure contains   a <a href="https://msdn.microsoft.com/d367bb85-514d-4acc-b67f-f7381a9a6404">WS_HEAP_PROPERTIES</a> structure.
                

The following heap properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_MAX_SIZE</a>.  If not specified, the
                    default value used is 256k bytes.
                    </li>
<li>
<a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_TRIM_SIZE</a>.  If not specified, the
                    default value used is 32k bytes.
                </li>
</ul>

### -field WS_METADATA_PROPERTY_POLICY_PROPERTIES

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a> to specify
                    properties of the <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> objects that are associated
                    with the metadata object.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> structure contains   a <a href="https://msdn.microsoft.com/e03f94d9-aeeb-40df-a367-c80e831125e8">WS_POLICY_PROPERTIES</a>  structure that specifies the
                    set of policy properties.

See <a href="https://msdn.microsoft.com/503d39c0-7546-429d-b8e3-66e80c76b7c1">WS_POLICY_PROPERTY_ID</a> for more information on the
                    set of properties that may be specified here.
                


### -field WS_METADATA_PROPERTY_HEAP_REQUESTED_SIZE

This property is used with <a href="https://msdn.microsoft.com/21d8dbca-e8a5-4b2f-a1f7-951532922024">WsGetMetadataProperty</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> is a <b>SIZE_T</b> specifying the number of bytes allocated from the heap associated with the
                    metadata object.


### -field WS_METADATA_PROPERTY_MAX_DOCUMENTS

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> is a <b>ULONG</b> specifying  the maximum number of documents that may be added to
                    the metadata object using <a href="https://msdn.microsoft.com/0b824948-e06d-482d-8d53-c4e27d1ecf0f">WsReadMetadata</a>.  
                

The default value is 32.
                


### -field WS_METADATA_PROPERTY_HOST_NAMES

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> is a <a href="https://msdn.microsoft.com/9815eb1e-0ce6-4b56-9f9a-e3938d502b72">WS_HOST_NAMES</a> structure.
                

This property may only be specified if <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_VERIFY_HOST_NAMES</a> is <b>TRUE</b>.
                

See <a href="https://msdn.microsoft.com/7854fb44-c397-4fd0-8a0e-ea293eba4f01">WsGetMissingMetadataDocumentAddress</a> for more information
                    on verifying host names.
                

If the property is not specified, then the list of host names is empty.
                


### -field WS_METADATA_PROPERTY_VERIFY_HOST_NAMES

This property is used with <a href="https://msdn.microsoft.com/c3b6f926-331b-46a7-8180-36762abf63d7">WsCreateMetadata</a>.
                

The accompanying <b>value</b> member of the <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> is a <b>BOOL</b> that specifies whether or not host names should be verified.
                

See <a href="https://msdn.microsoft.com/7854fb44-c397-4fd0-8a0e-ea293eba4f01">WsGetMissingMetadataDocumentAddress</a> for more information
                    on verifying host names.
                

The default value is <b>TRUE</b>.
                

Setting this value to <b>FALSE</b> may cause an application to use
                    an address returned from <a href="https://msdn.microsoft.com/7854fb44-c397-4fd0-8a0e-ea293eba4f01">WsGetMissingMetadataDocumentAddress</a>that is from a host that it is not willing to accept metadata from.
                

