---
UID: NF:strmif.IDistributorNotify.Pause
title: IDistributorNotify::Pause
author: windows-sdk-content
description: The Pause method is called when the filter graph is entering a paused state.
old-location: dshow\idistributornotify_pause.htm
tech.root: DirectShow
ms.assetid: d8fcb5c0-4530-4084-adba-170a647588b1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDistributorNotify interface [DirectShow],Pause method, IDistributorNotify.Pause, IDistributorNotify::Pause, IDistributorNotifyPause, Pause, Pause method [DirectShow], Pause method [DirectShow],IDistributorNotify interface, dshow.idistributornotify_pause, strmif/IDistributorNotify::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDistributorNotify.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDistributorNotify::Pause


## -description



The <code>Pause</code> method is called when the filter graph is entering a paused state.




## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Transition is not complete, but no error has occurred.

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
</table>
 




## -remarks



This method is called before the filters are notified.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c7c9ee95-9d68-45c5-a3ca-8d6071782851">IDistributorNotify Interface</a>
 

 

