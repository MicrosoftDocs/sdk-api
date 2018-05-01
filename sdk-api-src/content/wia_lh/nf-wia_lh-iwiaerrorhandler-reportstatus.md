---
UID: NF:wia_lh.IWiaErrorHandler.ReportStatus
title: IWiaErrorHandler::ReportStatus method
author: windows-driver-content
description: The ReportStatus method displays information about an error or status during a transfer. In some cases this method allows the user to recover from an error.
old-location: image\iwiaerrorhandler_reportstatus.htm
old-project: image
ms.assetid: c244d5a1-d3c1-4f8f-9b55-3729e5f13887
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaErrorHandler, IWiaErrorHandler interface [Imaging Devices], ReportStatus method, IWiaErrorHandler::ReportStatus, IWiaErrorHandler_39808ebb-728b-40de-bdc0-48dd6614e59b.xml, ReportStatus method [Imaging Devices], ReportStatus method [Imaging Devices], IWiaErrorHandler interface, ReportStatus,IWiaErrorHandler.ReportStatus, image.iwiaerrorhandler_reportstatus, wia_lh/IWiaErrorHandler::ReportStatus
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
-	IWiaErrorHandler.ReportStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaErrorHandler::ReportStatus method


## -description


The <b>ReportStatus</b> method displays information about an error or status during a transfer. In some cases this method allows the user to recover from an error.


## -parameters




### -param lFlags [in]

Currently unused. Should be set to zero. 


### -param hwndParent [in]

Caller supplied handle of the window that should be used as the parent window for any dialog boxes. If this is set to <b>NULL</b>, no dialog boxes should be displayed.


### -param pWiaItem2 [in]

Pointer to the <b>IWiaItem2</b> item being transferred. <b>IWiaItem2</b> is described in the Microsoft Windows SDK documentation.


### -param hrStatus [in]

HRESULT variable that contains the status code received by the WIA transfer method, for example the <b>IWiaDataCallback::BandedDataCallback</b> method (described in the Windows SDK documentation).


### -param lPercentComplete [in]

Size of the data, in bytes, the <i>pbData</i> pointer refers to.


## -returns



Returns a standard COM error code if the error cannot be recovered from, or if the user chooses to abort the transfer in response to the displayed dialog box. There is additional information on the return values in the remarks section. Otherwise this method returns one of the following values:

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
Appropriate action was taken to correct the error and the transfer can continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No action was taken to handle the error or report status to the user.

</td>
</tr>
</table>
 




## -remarks



The COM proxy callback object (described in the Windows SDK documentation) calls the <b>WiaErrorHandler::ReportStatus</b> method when the driver sends an IT_MSG_DEVICE_STATUS message to the <b>IWiaDataCallback::BandedDataCallback</b> method (described in the Windows SDK documentation). The dialog box that this method displays provides the user with error or status information and possibly gives an opportunity to recover from the error and continue the transfer. The UI should provide only an informational dialog box and a chance to cancel the transfer if the HRESULT is SEVERITY_SUCCESS.

A driver that implements this method, should display a modal dialog box, owned by <i>hwndParent</i>, in response to a value of <i>hrStatus</i> for which <b>FAILED</b>(<i>hrStatus</i>) evaluates to <b>TRUE</b>. If <b>FAILED</b>(<i>hrStatus</i>) evaluates to <b>FALSE</b>, the value in <i>hrStatus</i> represents a nonfatal delay, and the dialog box displayed should be modeless. The dialog box should be removed when the status of the transfer changes. An error handler should return S_FALSE for unknown values of <i>hrStatus</i>.

The <i>hrStatus</i> parameter is set to WIA_STATUS_TRANSFER_BEGIN to inform the handler that a transfer has started. It is set to WIA_STATUS_TRANSFER_END when the transfer is complete.

If <i>hrStatus</i> is S_OK, the data transfer has resumed and no delay or error is currently in effect.




## -see-also




<a href="https://msdn.microsoft.com/b441fbca-75fe-4b9d-a9d5-2ad5a4a55801">IWiaErrorHandler</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543904">IWiaErrorHandler::GetStatusDescription</a>
 

 

