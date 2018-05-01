---
UID: NF:wia_lh.IWiaErrorHandler.GetStatusDescription
title: IWiaErrorHandler::GetStatusDescription method
author: windows-driver-content
description: The system UI calls the GetStatusDescription method to provide the user with extra information about an error, if the user requests this information. This method is implemented by a driver's UI extension.
old-location: image\iwiaerrorhandler_getstatusdescription.htm
old-project: image
ms.assetid: c3b5622d-9d51-4008-abb0-c8a60c4a6b16
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetStatusDescription method [Imaging Devices], GetStatusDescription method [Imaging Devices], IWiaErrorHandler interface, GetStatusDescription,IWiaErrorHandler.GetStatusDescription, IWiaErrorHandler, IWiaErrorHandler interface [Imaging Devices], GetStatusDescription method, IWiaErrorHandler::GetStatusDescription, IWiaErrorHandler_4bd0cba6-d729-4942-b56a-588af88ef913.xml, image.iwiaerrorhandler_getstatusdescription, wia_lh/IWiaErrorHandler::GetStatusDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wia_lh.h
req.include-header: Wia.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wia_lh.h
api_name:
-	IWiaErrorHandler.GetStatusDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaErrorHandler::GetStatusDescription method


## -description


 The system UI calls the <b>GetStatusDescription</b> method to provide the user with extra information about an error, if the user requests this information. This method is implemented by a driver's UI extension.


## -parameters




### -param lFlags [in]

Currently unused. Should be set to zero. 


### -param pWiaItem2 [in]

Pointer to the <b>IWiaItem2</b> item being transferred. <b>IWiaItem2</b> is described in the Microsoft Windows SDK documentation.


### -param hrStatus [in]

HRESULT variable that contains the status code received by the WIA transfer method, for example the <b>IWiaDataCallback::BandedDataCallback</b> method (described in the Windows SDK documentation).


### -param pbstrDescription [out]

Pointer to a BSTR that receives a description of the status or error encountered during the transfer. This parameter cannot be <b>NULL</b>. The driver must allocate the string using the <b>SysAllocString</b> function and the caller must free the string using the <b>SysFreeString</b> function. The <b>SysFreeString</b> and <b>SysAllocString </b>functions are described in the Windows SDK documentation.


## -returns



Returns a standard COM error code if an error occurs, or one of the following:

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
The<i> pbstrDescription</i> parameter contains a valid BSTR pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WIA_STATUS_NOT_HANDLED</b></dt>
</dl>
</td>
<td width="60%">
The value in the <i>hrStatus</i> parameter is unknown to the extension and no description is available.

</td>
</tr>
</table>
 




## -remarks



In order for an application to call <b>IWiaErrorHandler::GetStatusDescription</b>, the application must call <b>IWiaItem2::GetExtension</b> first to receive an interface pointer to the error handling extension. An application must pass "ErrorHandler" as bstrName and IID_IWiaErrorHandler as riidExtensionInterface. An application should pass 0 as lFlags to ensure upward compatibility.

The implementation of <b>IWiaErrorHandler::GetStatusDescription</b> should return S_OK for all the device status codes (<i>hrStatus</i>) that the implementation of <b>IWiaErrorHandler::ReportStatus </b>handles, and WIA_STATUS_NOT_HANDLED for those that <b>IWiaErrorHandler::ReportStatus </b>does not handle.




## -see-also




<a href="https://msdn.microsoft.com/b441fbca-75fe-4b9d-a9d5-2ad5a4a55801">IWiaErrorHandler</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543909">IWiaErrorHandler::ReportStatus</a>
 

 

