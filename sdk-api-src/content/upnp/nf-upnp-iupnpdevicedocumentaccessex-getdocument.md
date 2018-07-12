---
UID: NF:upnp.IUPnPDeviceDocumentAccessEx.GetDocument
title: IUPnPDeviceDocumentAccessEx::GetDocument
author: windows-sdk-content
description: Retrieves the XML device description document for a UPnP device.
old-location: upnp\iupnpdevicedocumentex_getdocument.htm
old-project: upnp
ms.assetid: 12778bd4-9e62-42a4-b9b3-29ee9c6d2d40
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetDocument, GetDocument method [UPnP APIs], GetDocument method [UPnP APIs],IUPnPDeviceDocumentAccessEx interface, IUPnPDeviceDocumentAccessEx interface [UPnP APIs],GetDocument method, IUPnPDeviceDocumentAccessEx.GetDocument, IUPnPDeviceDocumentAccessEx::GetDocument, upnp.iupnpdevicedocumentex_getdocument, upnp/IUPnPDeviceDocumentAccessEx::GetDocument
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceDocumentAccessEx.GetDocument
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceDocumentAccessEx::GetDocument


## -description


The <b>GetDocument</b> method retrieves the XML device description document for a UPnP device.


## -parameters




### -param pbstrDocument






#### - [out, retval]

Receives the XML device description document for the device.

After obtaining the XML device document, the memory for this parameter must be free by passing it to SysFreeString.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



<div class="alert"><b>Note</b>  This method does not support scripting.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9ea79bbb-3841-4704-9606-56fcd2f8bf89">IUPnPDeviceDocumentAccessEx</a>
 

 

