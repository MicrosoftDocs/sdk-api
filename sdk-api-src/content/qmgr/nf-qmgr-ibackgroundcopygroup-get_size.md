---
UID: NF:qmgr.IBackgroundCopyGroup.get_Size
title: IBackgroundCopyGroup::get_Size
author: windows-sdk-content
description: Use the get_Size method to retrieve the size of all files in the group to download.
old-location: bits\ibackgroundcopygroup_get_size.htm
tech.root: Bits
ms.assetid: 69190b6a-6920-4f84-9109-12079f00a6ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyGroup interface [BITS],get_Size method, IBackgroundCopyGroup.get_Size, IBackgroundCopyGroup::get_Size, bits.ibackgroundcopygroup_get_size, get_Size, get_Size method [BITS], get_Size method [BITS],IBackgroundCopyGroup interface, qmgr/IBackgroundCopyGroup::get_Size
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
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyGroup.get_Size
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyGroup::get_Size


## -description


<p class="CCE_Message">[<b>IBackgroundCopyGroup</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/72668c9b-e6f3-4f3f-9d4b-50d930d1889d">BITS interfaces</a>.]

Use the <b>get_Size</b> method to retrieve the size of all files in the group to download.


## -parameters




### -param pdwSize [out]

Total size, in bytes, of all files in the group to download, or 0 if QMGR cannot determine the size.


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
Successfully retrieved the size of the group.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/51ddd89a-489a-4b83-ad45-838809a6d2e8">IBackgroundCopyGroup</a>
 

 

