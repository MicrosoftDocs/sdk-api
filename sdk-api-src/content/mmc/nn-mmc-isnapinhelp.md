---
UID: NN:mmc.ISnapinHelp
title: ISnapinHelp (mmc.h)

description: Allows snap-ins to add HTML Help support.
old-location: mmc\isnapinhelp.htm
tech.root: mmc
ms.assetid: 237E52F7-5EB9-45DA-ACC3-391ED3BF7C5E

ms.date: 12/05/2018
ms.keywords: ISnapinHelp, ISnapinHelp interface [MMC], ISnapinHelp interface [MMC],described, mmc.isnapinhelp, mmc/ISnapinHelp
ms.topic: interface
f1_keywords: 
 - "mmc/ISnapinHelp"
dev_langs:
 - c++
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
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
 - Mmc.h
api_name:
 - ISnapinHelp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISnapinHelp interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Allows snap-ins to add HTML Help support.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinHelp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinHelp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinHelp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/mmc/nf-mmc-isnapinhelp-gethelptopic">GetHelpTopic</a>
</td>
<td align="left" width="63%">
Merges the snap-in's HTML Help file into the MMC HTML Help file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/adding-html-help-support">Adding HTML Help Support</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
 

 

