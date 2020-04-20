---
UID: NF:strmif.IDvdControl2.AcceptParentalLevelChange
title: IDvdControl2::AcceptParentalLevelChange (strmif.h)
description: The AcceptParentalLevelChange method accepts or rejects a request from the DVD Navigator to play content at a higher parental management level.helpviewer_keywords: ["AcceptParentalLevelChange","AcceptParentalLevelChange method [DirectShow]","AcceptParentalLevelChange method [DirectShow]","IDvdControl2 interface","IDvdControl2 interface [DirectShow]","AcceptParentalLevelChange method","IDvdControl2.AcceptParentalLevelChange","IDvdControl2::AcceptParentalLevelChange","IDvdControl2AcceptParentalLevelChange","dshow.idvdcontrol2_acceptparentallevelchange","strmif/IDvdControl2::AcceptParentalLevelChange"]
old-location: dshow\idvdcontrol2_acceptparentallevelchange.htm
tech.root: DirectShow
ms.assetid: a990544e-6600-44b1-91f2-8b88fa43ccaf
ms.date: 12/05/2018
ms.keywords: AcceptParentalLevelChange, AcceptParentalLevelChange method [DirectShow], AcceptParentalLevelChange method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],AcceptParentalLevelChange method, IDvdControl2.AcceptParentalLevelChange, IDvdControl2::AcceptParentalLevelChange, IDvdControl2AcceptParentalLevelChange, dshow.idvdcontrol2_acceptparentallevelchange, strmif/IDvdControl2::AcceptParentalLevelChange
f1_keywords:
- strmif/IDvdControl2.AcceptParentalLevelChange
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdControl2.AcceptParentalLevelChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::AcceptParentalLevelChange


## -description



The <code>AcceptParentalLevelChange</code> method accepts or rejects a request from the DVD Navigator to play content at a higher parental management level.




## -parameters




### -param bAccept [in]

Flag that indicates whether the application accepts the parental management level change. Specify <b>TRUE</b> to accept the change and play the higher-level content, or <b>FALSE</b> to reject the change.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



A temporary parental management level (PML) command is a marker on the DVD disc indicating that the content that follows has a PML higher than the level specified for the title as a whole. This marker also contains instructions on where to branch depending on whether the change is accepted or rejected. If you specify <b>FALSE</b>, the DVD Navigator follows the rejected branch on the disc. If you specify <b>TRUE</b>, the DVD Navigator follows the branch to the higher-level content.

Use <code>AcceptParentalLevelChange</code> in conjunction with the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">SetOption</a> method. The sequence of events is as follows: First, call <b>SetOption</b>(DVD_NotifyParentalLevelChange, <b>TRUE</b>) to tell the DVD Navigator to always wait after sending an EC_DVD_PARENTAL_LEVEL_CHANGE event notification to the application. In your event handler, implement code to determine whether to accept or reject the change, and then call <code>AcceptParentalLevelChange</code> to notify the DVD Navigator of the decision.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>All</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/enforcing-parental-management-levels">Enforcing Parental Management Levels</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

