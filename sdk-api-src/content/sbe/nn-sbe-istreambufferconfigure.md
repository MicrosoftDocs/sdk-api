---
UID: NN:sbe.IStreamBufferConfigure
title: IStreamBufferConfigure (sbe.h)
description: The IStreamBufferConfigure interface configures the location, number, and size of the backing files used by the various stream buffer objects.The StreamBufferConfig object exposes this interface.Before calling any of the Set methods on this interface, you must specify a registry key to hold the new settings. For more information, see IStreamBufferInitialize::SetHKEY.
old-location: mstv\istreambufferconfigure.htm
tech.root: mstv
ms.assetid: 8874fefd-2241-4b04-a7d5-191e13743fa0
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure, IStreamBufferConfigure interface [Microsoft TV Technologies], IStreamBufferConfigure interface [Microsoft TV Technologies],described, IStreamBufferConfigureInterface, mstv.istreambufferconfigure, sbe/IStreamBufferConfigure
f1_keywords:
- sbe/IStreamBufferConfigure
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Sbe.h
api_name:
- IStreamBufferConfigure
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferConfigure interface


## -description



The <b>IStreamBufferConfigure</b> interface configures the location, number, and size of the backing files used by the various stream buffer objects.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/streambufferconfig-object">StreamBufferConfig</a> object exposes this interface.

Before calling any of the <b>Set</b> methods on this interface, you must specify a registry key to hold the new settings. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferinitialize-sethkey">IStreamBufferInitialize::SetHKEY</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferConfigure</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-getbackingfilecount">GetBackingFileCount</a>
</td>
<td align="left" width="63%">
Retrieves the maximum and minimum number of backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-getbackingfileduration">GetBackingFileDuration</a>
</td>
<td align="left" width="63%">
Retrieves the backing file size, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-getdirectory">GetDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the directory where backing files are saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-setbackingfilecount">SetBackingFileCount</a>
</td>
<td align="left" width="63%">
Sets the maximum and minimum number of backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-setbackingfileduration">SetBackingFileDuration</a>
</td>
<td align="left" width="63%">
Sets the backing file size, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferconfigure-setdirectory">SetDirectory</a>
</td>
<td align="left" width="63%">
Sets the directory where backing files are saved.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

