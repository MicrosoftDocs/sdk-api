---
UID: NF:qmgr.IBackgroundCopyGroup.SwitchToForeground
title: IBackgroundCopyGroup::SwitchToForeground
author: windows-sdk-content
description: Use the SwitchToForeground method to download the group in the foreground instead of the background.
old-location: bits\ibackgroundcopygroup_switchtoforeground.htm
old-project: Bits
ms.assetid: 19619a97-b4f2-4609-9b06-bb188e00860c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],SwitchToForeground method, IBackgroundCopyGroup.SwitchToForeground, IBackgroundCopyGroup::SwitchToForeground, SwitchToForeground, SwitchToForeground method [BITS], SwitchToForeground method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_switchtoforeground, qmgr/IBackgroundCopyGroup::SwitchToForeground
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: GROUPPROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.SwitchToForeground
product: Windows
targetos: Windows
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
req.product: ADAM
---

# IBackgroundCopyGroup::SwitchToForeground


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>SwitchToForeground</b> method to download the group in the foreground instead of the background. 


## -parameters






## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Successfully switched the group to foreground processing.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

