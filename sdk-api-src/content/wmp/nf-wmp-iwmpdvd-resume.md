---
UID: NF:wmp.IWMPDVD.resume
title: IWMPDVD::resume method
author: windows-driver-content
description: The resume method returns to playback mode from menu mode at the same title position as when the menu was invoked.
old-location: wmp\iwmpdvd_resume.htm
old-project: WMP
ms.assetid: c0817edb-49af-48b8-82d0-a8c0a827f290
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPDVD, IWMPDVD interface [Windows Media Player], resume method, IWMPDVD::resume, IWMPDVDresume, resume method [Windows Media Player], resume method [Windows Media Player], IWMPDVD interface, resume,IWMPDVD.resume, wmp.iwmpdvd_resume, wmp/IWMPDVD::resume
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPDVD.resume
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPDVD::resume method


## -description



The <b>resume</b> method returns to playback mode from menu mode at the same title position as when the menu was invoked.




## -parameters






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



<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not perform the intended operation.




## -see-also




<a href="https://msdn.microsoft.com/d133f1e1-cbeb-403d-b247-9f495cb6f0f7">IWMPDVD Interface</a>
 

 

