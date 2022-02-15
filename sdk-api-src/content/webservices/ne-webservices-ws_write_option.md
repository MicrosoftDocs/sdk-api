---
UID: NE:webservices.__unnamed_enum_87
title: WS_WRITE_OPTION (webservices.h)
description: Specifies whether a storage specified contains the value, or a pointer to the value, and whether the value can be represented as nil in the XML content.
helpviewer_keywords: ["WS_WRITE_NILLABLE_POINTER","WS_WRITE_NILLABLE_VALUE","WS_WRITE_OPTION","WS_WRITE_OPTION enumeration [Web Services for Windows]","WS_WRITE_REQUIRED_POINTER","WS_WRITE_REQUIRED_VALUE","webservices/WS_WRITE_NILLABLE_POINTER","webservices/WS_WRITE_NILLABLE_VALUE","webservices/WS_WRITE_OPTION","webservices/WS_WRITE_REQUIRED_POINTER","webservices/WS_WRITE_REQUIRED_VALUE","wsw.ws_write_option"]
old-location: wsw\ws_write_option.htm
tech.root: wsw
ms.assetid: 24a0ad2c-fcec-42c5-8f72-bea431b06d2e
ms.date: 12/05/2018
ms.keywords: WS_WRITE_NILLABLE_POINTER, WS_WRITE_NILLABLE_VALUE, WS_WRITE_OPTION, WS_WRITE_OPTION enumeration [Web Services for Windows], WS_WRITE_REQUIRED_POINTER, WS_WRITE_REQUIRED_VALUE, webservices/WS_WRITE_NILLABLE_POINTER, webservices/WS_WRITE_NILLABLE_VALUE, webservices/WS_WRITE_OPTION, webservices/WS_WRITE_REQUIRED_POINTER, webservices/WS_WRITE_REQUIRED_VALUE, wsw.ws_write_option
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
targetos: Windows
req.typenames: WS_WRITE_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_WRITE_OPTION
 - webservices/WS_WRITE_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_WRITE_OPTION
---

# WS_WRITE_OPTION enumeration


## -description

Specifies whether a storage specified contains the value, or a pointer to the value,
                and whether the value can be represented as nil in the XML content.

## -enum-fields

### -field WS_WRITE_REQUIRED_VALUE:1

The storage specified contains the value.  The size of the storage 
                    specified should be the size of the value.
                

This option specifies that the value will always be written to the XML content.
                


``` syntax
int value;
Api(..., &amp;value, sizeof(value), ...);
```


``` syntax
// always written
&lt;element&gt;123&lt;/element&gt;
```

This option is not supported for pointer types
                    (<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a> and <b>WS_XML_BUFFER_TYPE</b>).  
                    The <a href="/windows/desktop/api/webservices/ne-webservices-ws_write_option">WS_WRITE_REQUIRED_POINTER</a> option should be used for these types.

### -field WS_WRITE_REQUIRED_POINTER:2

The storage specified contains a pointer to the value.  The
                    size of the storage specified is always the size of a pointer, regardless
                    of the type being serialized.
                

This option specifies that the value will always be written to the XML content.
                


``` syntax
int* valuePointer; // may not be NULL
Api(..., &amp;valuePointer, sizeof(valuePointer), ...);
```


``` syntax
// always written
&lt;element&gt;123&lt;/element&gt;
```

If the pointer to the value specified in the storage is <b>NULL</b>, 
                    <b>E_INVALIDARG</b> is returned.
                (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

### -field WS_WRITE_NILLABLE_VALUE:3

The storage specified contains a pointer to the value.  The
                    size of the storage specified is always the size of a pointer, regardless
                    of the type being serialized.
                

If the value is nil, then a nil element is written in the XML content.
                    If non-nil, then the value is serialized normally.
                


``` syntax
WS_STRING value; // may contain a nil value (see WS_STRING_TYPE)
Api(..., &amp;value, sizeof(value), ...);
```


``` syntax
// if value is non-nil
&lt;element&gt;hello&lt;/element&gt;

// if value is nil
&lt;element xsi:nil='true'/&gt;
```

This option is only supported for the following types, listed below,
                    which have a intrinsic way to represent a nil value.  See the documentation
                    for each type for information on how nil is represented.
                    <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_BYTES_TYPE</a>
</li>
</ul>

### -field WS_WRITE_NILLABLE_POINTER:4

For all types, the storage specified contains a pointer to the value.  The
                    size of the storage specified is always the size of a pointer, regardless
                    of the type being serialized.
                

If the pointer to the value specified in the storage is <b>NULL</b>, then
                    a nil element is written in the XML content.
                


``` syntax
int* valuePointer; // may be NULL
Api(..., &amp;valuePointer, sizeof(valuePointer), ...);

```


``` syntax
// if value is non-NULL
&lt;element&gt;123&lt;/element&gt;

// if value is NULL
&lt;element xsi:nil='true'/&gt;
```

