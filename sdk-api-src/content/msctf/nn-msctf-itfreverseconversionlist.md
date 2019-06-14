---
UID: NN:msctf.ITfReverseConversionList
title: ITfReverseConversionList (msctf.h)
author: windows-sdk-content
description: Represents a list of the keystroke sequences required to create a specified string.
old-location: tsf\itfreverseconversionlist.htm
tech.root: TSF
ms.assetid: 2659bade-af85-42c5-bdb3-32eab16753a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfReverseConversionList, ITfReverseConversionList interface [Text Services Framework], ITfReverseConversionList interface [Text Services Framework],described, msctf/ITfReverseConversionList, tsf.itfreverseconversionlist
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfReverseConversionList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITfReverseConversionList interface


## -description


<p class="CCE_Message">[<b>ITfReverseConversionList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Represents a list of the keystroke sequences required to create a specified string. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfReverseConversionList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfReverseConversionList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfReverseConversionList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionlist-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Retrieves the number of keystroke sequences in the list.

<div class="alert"><b>Note</b>  <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionlist-getlength">GetLength</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionlist-getstring">GetString</a>
</td>
<td align="left" width="63%">
Retrieves the keystroke sequence at the specified index. 

<div class="alert"><b>Note</b>  <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversionlist-getstring">GetString</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.</div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



This interface is used to store the results of the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfreverseconversion-doreverseconversion">ITfReverseConversionList::DoReverseConversion</a> method.



