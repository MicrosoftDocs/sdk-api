---
UID: NF:mfidl.IMFSchemeHandler.CancelObjectCreation
title: IMFSchemeHandler::CancelObjectCreation
author: windows-sdk-content
description: Cancels the current request to create an object from a URL.
old-location: mf\imfschemehandler_cancelobjectcreation.htm
old-project: medfound
ms.assetid: 662a4c47-95f8-4a84-ab2b-96e51d13906c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 662a4c47-95f8-4a84-ab2b-96e51d13906c, CancelObjectCreation, CancelObjectCreation method [Media Foundation], CancelObjectCreation method [Media Foundation],IMFSchemeHandler interface, IMFSchemeHandler interface [Media Foundation],CancelObjectCreation method, IMFSchemeHandler.CancelObjectCreation, IMFSchemeHandler::CancelObjectCreation, mf.imfschemehandler_cancelobjectcreation, mfidl/IMFSchemeHandler::CancelObjectCreation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSchemeHandler.CancelObjectCreation
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSchemeHandler::CancelObjectCreation


## -description



Cancels the current request to create an object from a URL.




## -parameters




### -param pIUnknownCancelCookie [in]

Pointer to the <b>IUnknown</b> interface that was returned in the <i>ppIUnknownCancelCookie</i> parameter of the <a href="https://msdn.microsoft.com/78858e8c-0eb3-4b62-84f0-76e9dff0e3ce">IMFSchemeHandler::BeginCreateObject</a> method.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



You can use this method to cancel a previous call to <a href="https://msdn.microsoft.com/78858e8c-0eb3-4b62-84f0-76e9dff0e3ce">BeginCreateObject</a>. Because that method is asynchronous, however, it might be completed before the operation can be canceled. Therefore, your callback might still be invoked after you call this method.

The operation cannot be canceled if <a href="https://msdn.microsoft.com/78858e8c-0eb3-4b62-84f0-76e9dff0e3ce">BeginCreateObject</a> returns <b>NULL</b> in the <i>ppIUnknownCancelCookie</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/a342054e-2cb5-494a-a2f7-d144c72d1fa5">IMFSchemeHandler</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

