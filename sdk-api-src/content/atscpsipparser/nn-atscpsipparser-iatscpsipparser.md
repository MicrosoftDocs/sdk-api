---
UID: NN:atscpsipparser.IAtscPsipParser
title: IAtscPsipParser (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAtscPsipParser interface retrieves ATSC Program and System Information Protocol (PSIP) tables.
old-location: mstv\iatscpsipparser.htm
tech.root: mstv
ms.assetid: dbe922b3-b843-4eaa-807d-5608cfbb9686
ms.date: 12/05/2018
ms.keywords: IAtscPsipParser, IAtscPsipParser interface [Microsoft TV Technologies], IAtscPsipParser interface [Microsoft TV Technologies],described, IAtscPsipParserInterface, atscpsipparser/IAtscPsipParser, mstv.iatscpsipparser
f1_keywords:
- atscpsipparser/IAtscPsipParser
dev_langs:
- c++
req.header: atscpsipparser.h
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
- atscpsipparser.h
api_name:
- IAtscPsipParser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAtscPsipParser interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAtscPsipParser</b> interface retrieves ATSC Program and System Information Protocol (PSIP) tables.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAtscPsipParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAtscPsipParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAtscPsipParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getcat">GetCAT</a>
</td>
<td align="left" width="63%">
Retrieves the conditional access table (CAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteas">GetEAS</a>
</td>
<td align="left" width="63%">
Retrieves the emergency alert message (EAS) table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteit">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getett">GetETT</a>
</td>
<td align="left" width="63%">
Retrieves the extended text table (ETT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getmgt">GetMGT</a>
</td>
<td align="left" width="63%">
Retrieves the master guide table (MGT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpat">GetPAT</a>
</td>
<td align="left" width="63%">
Retrieves the program association table (PAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpmt">GetPMT</a>
</td>
<td align="left" width="63%">
Retrieves the program map table (PMT) for a specified PID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getstt">GetSTT</a>
</td>
<td align="left" width="63%">
Retrieves the system time table (STT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-gettsdt">GetTSDT</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream description table (TSDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getvct">GetVCT</a>
</td>
<td align="left" width="63%">
Retrieves the virtual channel table (VCT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the ATSC PSIP parser.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:


```cpp
3508C064-B94E-420b-A821-20C8096FAADC
```


This CLSID is not is not published in an SDK header; define a new GUID constant in your application.

You must call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-initialize">Initialize</a> before calling any other methods on the object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

