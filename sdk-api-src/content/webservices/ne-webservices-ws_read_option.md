---
UID: NE:webservices.__unnamed_enum_86
title: WS_READ_OPTION (webservices.h)
description: Specifies whether a value is required, and how the value should be allocated.
old-location: wsw\ws_read_option.htm
tech.root: wsw
ms.assetid: 634b057f-3121-43cc-919f-8636e67ce0d7
ms.date: 12/05/2018
ms.keywords: WS_READ_NILLABLE_POINTER, WS_READ_NILLABLE_VALUE, WS_READ_OPTION, WS_READ_OPTION enumeration [Web Services for Windows], WS_READ_OPTIONAL_POINTER, WS_READ_REQUIRED_POINTER, WS_READ_REQUIRED_VALUE, webservices/WS_READ_NILLABLE_POINTER, webservices/WS_READ_NILLABLE_VALUE, webservices/WS_READ_OPTION, webservices/WS_READ_OPTIONAL_POINTER, webservices/WS_READ_REQUIRED_POINTER, webservices/WS_READ_REQUIRED_VALUE, wsw.ws_read_option
ms.topic: enum
f1_keywords:
- webservices/WS_READ_OPTION
dev_langs:
- c++
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
- WS_READ_OPTION
targetos: Windows
req.typenames: WS_READ_OPTION
req.redist: 
ms.custom: 19H1
---

# WS_READ_OPTION enumeration


## -description


Specifies whether a value is required, and how the value should be allocated.
            


## -enum-fields




### -field WS_READ_REQUIRED_VALUE

The option specifies that the value must exist in the XML content.
                

The caller must specify the storage to read the top-level type into.
                

The size of the storage specified by the caller varies by the type
                    being deserialized, as follows:
                    <ul>
<li>For primitives (such as <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_INT32_TYPE</a>), the storage should 
                        be the size of the primitive.  In this case, the heap does not need to be specified.
                        </li>
<li>For structures (whether user defined ones that use <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRUCT_TYPE</a>,
                        or predefined ones like <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_string">WS_STRING</a>), the storage should be the 
                        exact size of the structure.
                        Note that fields of the structure that point to other data is still required to
                        be allocated from the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>.  If no fields exist for the
                        specific structure, then the heap does not need to be specified.
                    </li>
</ul>


Pointer types (<a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a> and <b>WS_XML_BUFFER_TYPE</b>),
                    may not be used with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_VALUE</a>.  The <b>WS_READ_REQUIRED_POINTER</b>  
                    value should be used instead.
                

If the value is not present in the XML being read,  
                    a <b>WS_E_INVALID_FORMAT</b> error will be returned.
                (See <a href="https://docs.microsoft.com/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)


### -field WS_READ_REQUIRED_POINTER

The option specifies that the value must exist in the XML content.
                

The deserialized value is always allocated on the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                

If the value is not present, then an error will be returned.
                    <b>NULL</b> will never be returned when this option is used.  If the
                    value is optional, use <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_OPTIONAL_POINTER</a>.
                


### -field WS_READ_OPTIONAL_POINTER

The option specifies that the value need not exist in the XML content.
                

The deserialized value is always allocated on the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                

If the value is not present in the XML being read, the function will
                    succeed and <b>NULL</b> will be returned for the value.
                

An application that uses this option should be careful to check for <b>NULL</b> before accessing the value.
                    If a <b>NULL</b> value is never expected, use <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_POINTER</a>.
                


### -field WS_READ_NILLABLE_POINTER

The option specifies that the value may be nil or missing in the XML content.
                

The deserialized value is always allocated on the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                

If the element is nil or missing in the XML being read, the function will succeed and
                    a <b>NULL</b> pointer will be returned.  
                    If the element is not nil in the XML being read, then the value is returned normally.
                

An application that uses this option should be careful to check for <b>NULL</b> before accessing the value.
                    If a <b>NULL</b> value is never expected, use <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_read_option">WS_READ_REQUIRED_POINTER</a>.
                

This option is not supported in combination with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a> in APIs
                that read XML, inlcuding <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadtype">WsReadType</a> and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadelement">WsReadElement</a> calls.
              


### -field WS_READ_NILLABLE_VALUE

The option specifies that the value may be nil or missing in the XML content.
                

The caller must specify the storage to read the top-level type into.
                

If the XML element is nil or missing, then a nil value is returned.  If the XML element is
                    non-nil, then the value is deserialized normally.
                

This option is not supported in combination with <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type_mapping">WS_TYPE_MAPPING</a> in APIs
                that read XML, inlcuding <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadtype">WsReadType</a> and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsreadelement">WsReadElement</a> calls.
              

This option is only supported for the following types, listed below,
              which have a intrinsic way to represent a nil value.  See the documentation
              for each type for information on how nil is represented.
              <ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_BYTES_TYPE</a>
</li>
</ul>



## -remarks



Each <b>WS_READ_OPTION</b> discusses when a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>object must be specified.  Depending on the function, it may still be
                possible to pass a <b>NULL</b> heap parameter in this case; see the documentation
                for the specific function for details on whether a default heap is used
                if the heap parameter is <b>NULL</b>.
            

The following are things to consider when deserializing values into
                a heap object (<a href="https://docs.microsoft.com/windows/desktop/wsw/ws-heap">WS_HEAP</a>):
            

<ul>
<li>Deserialized values remain allocated until the heap
                is freed (<a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsfreeheap">WsFreeHeap</a>) or reset (<a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsresetheap">WsResetHeap</a>).
                </li>
<li>Each time values are deserialized, they are appended to the heap (instead
                of replacing existing values).
                </li>
<li>If errors are encountered during the deserialization function and the
                function fails, the memory allocated from the heap object up until 
                the error will not be released.
                </li>
<li>The size of the heap can be used to limit the total allocations made
                during deserialization.  The max size of the heap can be determined 
                in the following way:
                <ul>
<li>Determine the max size, in bytes, of each value that will be
                    allocated on the heap during deserialization. Remember to take into
                    account that sizes of deserialized data structures may vary by platform.
                    </li>
<li>Each array is considered one value.  Note that the actual size of an item
                    in the array may by affected by the required alignment of the item.
                    </li>
<li>Round the max size of each value to a 16-byte boundary.
                </li>
</ul>
</li>
</ul>


