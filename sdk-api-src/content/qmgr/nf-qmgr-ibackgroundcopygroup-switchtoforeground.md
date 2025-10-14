---
UID: NF:qmgr.IBackgroundCopyGroup.SwitchToForeground
title: IBackgroundCopyGroup::SwitchToForeground (qmgr.h)
description: Use the SwitchToForeground method to download the group in the foreground instead of the background.
helpviewer_keywords: ["IBackgroundCopyGroup interface [BITS]","SwitchToForeground method","IBackgroundCopyGroup.SwitchToForeground","IBackgroundCopyGroup::SwitchToForeground","SwitchToForeground","SwitchToForeground method [BITS]","SwitchToForeground method [BITS]","IBackgroundCopyGroup interface","bits.ibackgroundcopygroup_switchtoforeground","qmgr/IBackgroundCopyGroup::SwitchToForeground"]
old-location: bits\ibackgroundcopygroup_switchtoforeground.htm
tech.root: Bits
ms.assetid: 19619a97-b4f2-4609-9b06-bb188e00860c
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],SwitchToForeground method, IBackgroundCopyGroup.SwitchToForeground, IBackgroundCopyGroup::SwitchToForeground, SwitchToForeground, SwitchToForeground method [BITS], SwitchToForeground method [BITS],IBackgroundCopyGroup interface, bits.ibackgroundcopygroup_switchtoforeground, qmgr/IBackgroundCopyGroup::SwitchToForeground
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyGroup::SwitchToForeground
 - qmgr/IBackgroundCopyGroup::SwitchToForeground
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.SwitchToForeground
---

# IBackgroundCopyGroup::SwitchToForeground


## -description

<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>SwitchToForeground</b> method to download the group in the foreground instead of the background.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully switched the group to foreground processing.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopygroup">IBackgroundCopyGroup</a>
