---
UID: NF:strmif.IAMVfwCaptureDialogs.ShowDialog
title: IAMVfwCaptureDialogs::ShowDialog
author: windows-sdk-content
description: The ShowDialog method displays the specified VFW dialog box.
old-location: dshow\iamvfwcapturedialogs_showdialog.htm
old-project: DirectShow
ms.assetid: 988b68e5-12fb-47c5-8a49-81ba262da739
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMVfwCaptureDialogs interface [DirectShow],ShowDialog method, IAMVfwCaptureDialogs.ShowDialog, IAMVfwCaptureDialogs::ShowDialog, IAMVfwCaptureDialogsShowDialog, ShowDialog, ShowDialog method [DirectShow], ShowDialog method [DirectShow],IAMVfwCaptureDialogs interface, dshow.iamvfwcapturedialogs_showdialog, strmif/IAMVfwCaptureDialogs::ShowDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVfwCaptureDialogs.ShowDialog
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCaptureDialogs::ShowDialog


## -description



The <code>ShowDialog</code> method displays the specified VFW dialog box.




## -parameters




### -param iDialog [in]

Dialog box to display. This is a member of the <a href="https://msdn.microsoft.com/0465d887-6452-4a67-9f52-a459620d12d2">VfwCaptureDialogs</a> enumeration.


### -param hwnd [in]

Handle of the dialog box's parent window.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Could not reconnect with the new format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not stopped.

</td>
</tr>
</table>
 




## -remarks



Stop the filter graph before calling this method. Otherwise, the method fails and returns VFW_E_NOT_STOPPED.

The Video Format dialog (VfwCaptureDialog_Format) may change the video format. If so, the method tries to reconnect the capture filter. If the downstream filter rejects the new format, the method returns VFW_E_CANNOT_CONNECT.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5198c80c-28f3-4b5c-9b3b-aa502bf3a384">IAMVfwCaptureDialogs Interface</a>
 

 

