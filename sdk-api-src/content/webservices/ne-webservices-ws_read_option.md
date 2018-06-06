---
UID: NE:webservices.WS_READ_OPTION
title: WS_READ_OPTION
author: windows-sdk-content
description: Specifies whether a value is required, and how the value should be allocated.
old-location: wsw\ws_read_option.htm
old-project: wsw
ms.assetid: 634b057f-3121-43cc-919f-8636e67ce0d7
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_READ_NILLABLE_POINTER, WS_READ_NILLABLE_VALUE, WS_READ_OPTION, WS_READ_OPTION enumeration [Web Services for Windows], WS_READ_OPTIONAL_POINTER, WS_READ_REQUIRED_POINTER, WS_READ_REQUIRED_VALUE, webservices/WS_READ_NILLABLE_POINTER, webservices/WS_READ_NILLABLE_VALUE, webservices/WS_READ_OPTION, webservices/WS_READ_OPTIONAL_POINTER, webservices/WS_READ_REQUIRED_POINTER, webservices/WS_READ_REQUIRED_VALUE, wsw.ws_read_option
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_READ_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_READ_OPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
<li>
                        For primitives (such as <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_INT32_TYPE</a>), the storage should 
                        be the size of the primitive.  In this case, the heap does not need to be specified.
                        </li>
<li>
                        For structures (whether user defined ones that use <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRUCT_TYPE</a>,
                        or predefined ones like <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a>), the storage should be the 
                        exact size of the structure.
                        Note that fields of the structure that point to other data is still required to
                        be allocated from the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>.  If no fields exist for the
                        specific structure, then the heap does not need to be specified.
                    </li>
</ul>



                    Pointer types (<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_WSZ_TYPE</a> and <b>WS_XML_BUFFER_TYPE</b>),
                    may not be used with <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_REQUIRED_VALUE</a>.  The <b>WS_READ_REQUIRED_POINTER</b>  
                    value should be used instead.
                


                    If the value is not present in the XML being read,  
                    a <b>WS_E_INVALID_FORMAT</b> error will be returned.
                (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


### -field WS_READ_REQUIRED_POINTER


                    The option specifies that the value must exist in the XML content.
                


                    The deserialized value is always allocated on the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                


                    If the value is not present, then an error will be returned.
                    <b>NULL</b> will never be returned when this option is used.  If the
                    value is optional, use <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTIONAL_POINTER</a>.
                


### -field WS_READ_OPTIONAL_POINTER


                    The option specifies that the value need not exist in the XML content.
                


                    The deserialized value is always allocated on the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                


                    If the value is not present in the XML being read, the function will
                    succeed and <b>NULL</b> will be returned for the value.
                


                    An application that uses this option should be careful to check for <b>NULL</b> before accessing the value.
                    If a <b>NULL</b> value is never expected, use <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_REQUIRED_POINTER</a>.
                


### -field WS_READ_NILLABLE_POINTER


                    The option specifies that the value may be nil or missing in the XML content.
                


                    The deserialized value is always allocated on the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>, regardless of it's size.
                    The pointer to the deserialized value is returned.  When using this option,
                    the caller should pass the address of a pointer, and size of a pointer,
                    regardless of the type being deserialized.
                


                    If the element is nil or missing in the XML being read, the function will succeed and
                    a <b>NULL</b> pointer will be returned.  
                    If the element is not nil in the XML being read, then the value is returned normally.
                


                    An application that uses this option should be careful to check for <b>NULL</b> before accessing the value.
                    If a <b>NULL</b> value is never expected, use <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_REQUIRED_POINTER</a>.
                

This option is not supported in combination with <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> in APIs
                that read XML, inlcuding <a href="https://msdn.microsoft.com/6d026b2e-f2c2-4990-9178-152585a7749a">WsReadType</a> and <a href="https://msdn.microsoft.com/88e0cc4d-ae24-46af-998d-fdbfbcc1be64">WsReadElement</a> calls.
              


### -field WS_READ_NILLABLE_VALUE


                    The option specifies that the value may be nil or missing in the XML content.
                


                    The caller must specify the storage to read the top-level type into.
                


                    If the XML element is nil or missing, then a nil value is returned.  If the XML element is
                    non-nil, then the value is deserialized normally.
                


                This option is not supported in combination with <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> in APIs
                that read XML, inlcuding <a href="https://msdn.microsoft.com/6d026b2e-f2c2-4990-9178-152585a7749a">WsReadType</a> and <a href="https://msdn.microsoft.com/88e0cc4d-ae24-46af-998d-fdbfbcc1be64">WsReadElement</a> calls.
              


              This option is only supported for the following types, listed below,
              which have a intrinsic way to represent a nil value.  See the documentation
              for each type for information on how nil is represented.
              <ul>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_BYTES_TYPE</a>
</li>
</ul>



## -remarks




                Each <b>WS_READ_OPTION</b> discusses when a <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>
                object must be specified.  Depending on the function, it may still be
                possible to pass a <b>NULL</b> heap parameter in this case; see the documentation
                for the specific function for details on whether a default heap is used
                if the heap parameter is <b>NULL</b>.
            


                The following are things to consider when deserializing values into
                a heap object (<a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a>):
            

<ul>
<li>
                Deserialized values remain allocated until the heap
                is freed (<a href="https://msdn.microsoft.com/ec643915-8c4b-4916-b390-d6ca043350db">WsFreeHeap</a>) or reset (<a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a>).
                </li>
<li>
                Each time values are deserialized, they are appended to the heap (instead
                of replacing existing values).
                </li>
<li>
                If errors are encountered during the deserialization function and the
                function fails, the memory allocated from the heap object up until 
                the error will not be released.
                </li>
<li>
                The size of the heap can be used to limit the total allocations made
                during deserialization.  The max size of the heap can be determined 
                in the following way:
                <ul>
<li>
                    Determine the max size, in bytes, of each value that will be
                    allocated on the heap during deserialization. Remember to take into
                    account that sizes of deserialized data structures may vary by platform.
                    </li>
<li>
                    Each array is considered one value.  Note that the actual size of an item
                    in the array may by affected by the required alignment of the item.
                    </li>
<li>
                    Round the max size of each value to a 16-byte boundary.
                </li>
</ul>
</li>
</ul>


