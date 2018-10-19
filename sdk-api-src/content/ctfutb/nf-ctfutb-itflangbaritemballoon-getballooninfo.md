---
UID: NF:ctfutb.ITfLangBarItemBalloon.GetBalloonInfo
title: ITfLangBarItemBalloon::GetBalloonInfo
author: windows-sdk-content
description: ITfLangBarItemBalloon::GetBalloonInfo method
old-location: tsf\itflangbaritemballoon_getballooninfo.htm
tech.root: TSF
ms.assetid: 4cf695dc-dfb7-4541-a364-4395650f9419
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetBalloonInfo, GetBalloonInfo method [Text Services Framework], GetBalloonInfo method [Text Services Framework],ITfLangBarItemBalloon interface, ITfLangBarItemBalloon interface [Text Services Framework],GetBalloonInfo method, ITfLangBarItemBalloon.GetBalloonInfo, ITfLangBarItemBalloon::GetBalloonInfo, _tsf_itflangbaritemballoon_getballooninfo_ref, ctfutb/ITfLangBarItemBalloon::GetBalloonInfo, tsf.itflangbaritemballoon_getballooninfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemBalloon.GetBalloonInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBalloon::GetBalloonInfo


## -description




## -parameters




### -param pInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms629076(v=VS.85).aspx">TF_LBBALLOONINFO</a> structure that receives the information about the balloon.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pInfo</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms628702(v=VS.85).aspx">ITfLangBarItemBalloon</a>



<a href="https://msdn.microsoft.com/8ceed1ae-27f9-4998-b950-52865bfa2f79">TF_LBBALLOONINFO
      </a>
 

 

