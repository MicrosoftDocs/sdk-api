---
UID: NN:mpeg2psiparser.IPSITables
title: IPSITables (mpeg2psiparser.h)
author: windows-sdk-content
description: Gets an MPEG-2 program specific information (PSI) table from an MPEG-2 transport stream.
old-location: mstv\ipsitables.htm
tech.root: mstv
ms.assetid: 6f07b4d2-7a52-448c-9e9f-729bd5261757
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSITables, IPSITables interface [Microsoft TV Technologies], IPSITables interface [Microsoft TV Technologies],described, mpeg2psiparser/IPSITables, mstv.ipsitables
ms.topic: interface
f1_keywords: ["mpeg2psiparser/IPSITables"]
req.header: mpeg2psiparser.h
req.include-header: Mpeg2PsiParser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - mpeg2psiparser.h
api_name:
 - IPSITables
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPSITables interface


## -description


Gets an MPEG-2 program specific information (PSI) table from an MPEG-2 transport stream.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> (TIF) implements this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPSITables</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPSITables</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPSITables</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">GetTable</a>
</td>
<td align="left" width="63%">
Gets an MPEG-2 PSI table from an MPEG-2 transport stream.

</td>
</tr>
</table> 

