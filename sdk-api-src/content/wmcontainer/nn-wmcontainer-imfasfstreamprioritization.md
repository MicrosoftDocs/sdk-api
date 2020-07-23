---
UID: NN:wmcontainer.IMFASFStreamPrioritization
title: IMFASFStreamPrioritization (wmcontainer.h)
description: Not implemented.
helpviewer_keywords: ["6eb79c52-dc81-406c-9000-d25ad380e6b2","IMFASFStreamPrioritization","IMFASFStreamPrioritization interface [Media Foundation]","IMFASFStreamPrioritization interface [Media Foundation]","described","mf.imfasfstreamprioritization","wmcontainer/IMFASFStreamPrioritization"]
old-location: mf\imfasfstreamprioritization.htm
tech.root: mf
ms.assetid: 6eb79c52-dc81-406c-9000-d25ad380e6b2
ms.date: 12/05/2018
ms.keywords: 6eb79c52-dc81-406c-9000-d25ad380e6b2, IMFASFStreamPrioritization, IMFASFStreamPrioritization interface [Media Foundation], IMFASFStreamPrioritization interface [Media Foundation],described, mf.imfasfstreamprioritization, wmcontainer/IMFASFStreamPrioritization
f1_keywords:
- wmcontainer/IMFASFStreamPrioritization
dev_langs:
- c++
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFASFStreamPrioritization
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFStreamPrioritization interface


## -description


<div class="alert"><b>Note</b>  This interface is not implemented.</div><div> </div>Manages information about the relative priorities of a group of streams in an Advanced Systems Format (ASF) profile. This interface manages information about the relative priorities of a group of streams in an ASF profile. Priority is used in streaming to determine which streams should be dropped first when available bandwidth decreases.

The ASF stream prioritization object exposes this interface. The stream prioritization object maintains a list of stream numbers in priority order. The methods of this interface manipulate and interrogate that list. To obtain a pointer to this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstreamprioritization">IMFASFProfile::CreateStreamPrioritization</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFStreamPrioritization</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFStreamPrioritization</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFStreamPrioritization</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the stream prioritization object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves the stream number of a stream in the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the stream priority list.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamprioritization-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the stream priority list.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

