---
UID: NF:mfapi.MFUnlockPlatform
title: MFUnlockPlatform function
author: windows-driver-content
description: Unlocks the Media Foundation platform after it was locked by a call to the MFLockPlatform function.
old-location: mf\mfunlockplatform.htm
old-project: medfound
ms.assetid: d4ce5315-4bb2-4ca4-a9a0-20b638a43040
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MFUnlockPlatform, MFUnlockPlatform function [Media Foundation], d4ce5315-4bb2-4ca4-a9a0-20b638a43040, mf.mfunlockplatform, mfapi/MFUnlockPlatform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFUnlockPlatform
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFUnlockPlatform function


## -description



Unlocks the Media Foundation platform after it was locked by a call to the <a href="https://msdn.microsoft.com/040742dc-4ba3-4906-8257-65505b2924d5">MFLockPlatform</a> function.




## -parameters






## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



The application must call <b>MFUnlockPlatform</b> once for every call to <a href="https://msdn.microsoft.com/040742dc-4ba3-4906-8257-65505b2924d5">MFLockPlatform</a>.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/1eb20c44-58cb-4e34-a108-1b3c27d54ff1">Media Foundation Platform APIs</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

