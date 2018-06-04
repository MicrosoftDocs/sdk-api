---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
                

