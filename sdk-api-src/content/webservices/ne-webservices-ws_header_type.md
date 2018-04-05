---
UID: NE:webservices.WS_HEADER_TYPE
title: WS_HEADER_TYPE
author: windows-driver-content
description: Identifies a type of header.
old-location: wsw\ws_header_type.htm
old-project: wsw
ms.assetid: 4c9b927d-00c7-41e4-bc29-e84a4c23c162
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_ACTION_HEADER, WS_FAULT_TO_HEADER, WS_FROM_HEADER, WS_HEADER_TYPE, WS_HEADER_TYPE enumeration [Web Services for Windows], WS_MESSAGE_ID_HEADER, WS_RELATES_TO_HEADER, WS_REPLY_TO_HEADER, WS_TO_HEADER, webservices/WS_ACTION_HEADER, webservices/WS_FAULT_TO_HEADER, webservices/WS_FROM_HEADER, webservices/WS_HEADER_TYPE, webservices/WS_MESSAGE_ID_HEADER, webservices/WS_RELATES_TO_HEADER, webservices/WS_REPLY_TO_HEADER, webservices/WS_TO_HEADER, wsw.ws_header_type
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WS_HEADER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_HEADER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_HEADER_TYPE enumeration


## -description



                Identifies a type of header.
            


## -enum-fields




### -field WS_ACTION_HEADER


                    The Action addressing header.
                


                    This header can be used with the following <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_WSZ_TYPE</a>
</li>
</ul>



### -field WS_TO_HEADER


                    The To addressing header.
                


                    This header can be used with the following <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_WSZ_TYPE</a>
</li>
</ul>



### -field WS_MESSAGE_ID_HEADER


                    The MessageID addressing header.
                


                    This header can be used with the following <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_UNIQUE_ID_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_WSZ_TYPE</a>
</li>
</ul>



                    This header is not supported for <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>.
                


### -field WS_RELATES_TO_HEADER


                    The RelatesTo addressing header.
                


                    This header can be used with the following <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_UNIQUE_ID_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_WSZ_TYPE</a>
</li>
</ul>



                    This header is not supported for <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>.
                


### -field WS_FROM_HEADER


                    The From addressing header.
                


                    This header is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ENDPOINT_ADDRESS_TYPE</a>.
                


                    This header is not supported for <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>.
                


### -field WS_REPLY_TO_HEADER


                    The ReplyTo addressing header.
                


                    This header is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ENDPOINT_ADDRESS_TYPE</a>.
                


                    This header is not supported for <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>.
                


### -field WS_FAULT_TO_HEADER


                    The FaultTo addressing header, in <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> format.
                


                    This header is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ENDPOINT_ADDRESS_TYPE</a>.
                


                    This header is not supported for <a href="https://msdn.microsoft.com/87f60067-109c-456c-b060-33ab840872e0">WS_ADDRESSING_VERSION_TRANSPORT</a>.
                

