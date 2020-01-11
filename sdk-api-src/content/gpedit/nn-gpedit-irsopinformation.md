---
UID: NN:gpedit.IRSOPInformation
title: IRSOPInformation (gpedit.h)
description: The IRSOPInformation interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the main Resultant Set of Policy (RSoP) snap-in. For more information about MMC, see the Microsoft Management Console.
old-location: policy\irsopinformation.htm
tech.root: Policy
ms.assetid: e3662977-d7a7-47bc-989b-a820d4c05382
ms.date: 12/05/2018
ms.keywords: IRSOPInformation, IRSOPInformation interface [Group Policy], IRSOPInformation interface [Group Policy],described, _win32_irsopinformation, gpedit/IRSOPInformation, policy.irsopinformation
f1_keywords:
- gpedit/IRSOPInformation
dev_langs:
- c++
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Gpedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gpedit.dll
api_name:
- IRSOPInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRSOPInformation interface


## -description


The
    <b>IRSOPInformation</b> interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the main Resultant Set of Policy (RSoP) snap-in. For more information about MMC, see the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-programmer-s-guide">Microsoft Management Console</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRSOPInformation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRSOPInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRSOPInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-irsopinformation-geteventlogentrytext">GetEventLogEntryText</a>
</td>
<td align="left" width="63%">
Returns the text for a specific entry in the event log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-irsopinformation-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves information about the RSoP user interface session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-irsopinformation-getnamespace">GetNameSpace</a>
</td>
<td align="left" width="63%">
Retrieves the namespace from which the RSoP data is being displayed.

</td>
</tr>
</table> 

