---
UID: NN:bits5_0.IBackgroundCopyJob5
title: IBackgroundCopyJob5
author: windows-sdk-content
description: Use this interface to query or set several optional behaviors of a job.
old-location: bits\bits5_functions.htm
tech.root: bits
ms.assetid: 97481F9D-1F7B-473A-B288-A52E527478A0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBackgroundCopyJob5, IBackgroundCopyJob5 interface [BITS], IBackgroundCopyJob5 interface [BITS],described, bits.bits5_functions, bits.ibackgroundcopyjob5, bits5_0/IBackgroundCopyJob5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: Bitsprx7.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bitsprx7.dll
api_name:
 - IBackgroundCopyJob5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyJob5 interface


## -description


Use this interface to query or set several optional behaviors of a job.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using 
    <code>__uuidof(IBackgroundCopyJob5)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob5</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa362990(v=VS.85).aspx">IBackgroundCopyJob3</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa362995(v=VS.85).aspx">IBackgroundCopyJob4</a>. <b>IBackgroundCopyJob5</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh446786(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
A generic method for getting BITS job properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh404135(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
A generic method for setting BITS job properties.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362973(v=VS.85).aspx">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362981(v=VS.85).aspx">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362990(v=VS.85).aspx">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362995(v=VS.85).aspx">IBackgroundCopyJob4</a>
 

 

