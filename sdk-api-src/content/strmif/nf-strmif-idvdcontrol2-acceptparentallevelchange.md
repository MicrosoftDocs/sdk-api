---
UID: NF:strmif.IDvdControl2.AcceptParentalLevelChange
title: IDvdControl2::AcceptParentalLevelChange
author: windows-sdk-content
description: The AcceptParentalLevelChange method accepts or rejects a request from the DVD Navigator to play content at a higher parental management level.
old-location: dshow\idvdcontrol2_acceptparentallevelchange.htm
tech.root: DirectShow
ms.assetid: a990544e-6600-44b1-91f2-8b88fa43ccaf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AcceptParentalLevelChange, AcceptParentalLevelChange method [DirectShow], AcceptParentalLevelChange method [DirectShow],IDvdControl2 interface, IDvdControl2 interface [DirectShow],AcceptParentalLevelChange method, IDvdControl2.AcceptParentalLevelChange, IDvdControl2::AcceptParentalLevelChange, IDvdControl2AcceptParentalLevelChange, dshow.idvdcontrol2_acceptparentallevelchange, strmif/IDvdControl2::AcceptParentalLevelChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Use <code>AcceptParentalLevelChange</code> in conjunction with the <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">SetOption</a> method. The sequence of events is as follows: First, call <b>SetOption</b>(DVD_NotifyParentalLevelChange, <b>TRUE</b>) to tell the DVD Navigator to always wait after sending an EC_DVD_PARENTAL_LEVEL_CHANGE event notification to the application. In your event handler, implement code to determine whether to accept or reject the change, and then call <code>AcceptParentalLevelChange</code> to notify the DVD Navigator of the decision.

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




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/ad996a03-e94e-4743-90a2-aa390984a231">Enforcing Parental Management Levels</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

