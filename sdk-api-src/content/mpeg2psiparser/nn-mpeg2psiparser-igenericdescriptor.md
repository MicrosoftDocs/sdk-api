---
UID: NN:mpeg2psiparser.IGenericDescriptor
title: IGenericDescriptor (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\igenericdescriptor.htm
tech.root: mstv
ms.assetid: efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84
ms.date: 12/05/2018
ms.keywords: IGenericDescriptor, IGenericDescriptor interface [Microsoft TV Technologies], IGenericDescriptor interface [Microsoft TV Technologies],described, IGenericDescriptorInterface, mpeg2psiparser/IGenericDescriptor, mstv.igenericdescriptor
ms.topic: interface
f1_keywords:
- mpeg2psiparser/IGenericDescriptor
dev_langs:
- c++
req.header: mpeg2psiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- Mpeg2PsiParser.h
api_name:
- IGenericDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGenericDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IGenericDescriptor</b> enables the client to get an MPEG-2 descriptor in an unparsed format.

See ISO/IEC 1318-1 for the MPEG-2 descriptor specifications. See ETSI EN 300 468 for the DVB descriptor specifications.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGenericDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGenericDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGenericDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-igenericdescriptor-getbody">GetBody</a>
</td>
<td align="left" width="63%">
Returns the body of the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-igenericdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-igenericdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-igenericdescriptor-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

