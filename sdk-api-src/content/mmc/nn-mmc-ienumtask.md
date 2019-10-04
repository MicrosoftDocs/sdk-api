---
UID: NN:mmc.IEnumTASK
title: IEnumTASK (mmc.h)
author: windows-sdk-content
description: The IEnumTASK interface is introduced in MMC 1.1.
old-location: mmc\ienumtask.htm
tech.root: mmc
ms.assetid: 7cf1ff4f-bd45-4ead-a005-e0f38aed9039
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTASK, IEnumTASK interface [MMC], IEnumTASK interface [MMC],described, _slate_ienumtask, mmc.ienumtask, mmc/IEnumTASK
ms.topic: interface
f1_keywords: 
 - "mmc/IEnumTASK"
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
 - Mmc.h
api_name:
 - IEnumTASK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumTASK interface


## -description


The 
<b>IEnumTASK</b> interface is introduced in MMC 1.1.

The 
<b>IEnumTASK</b> interface enables a snap-in component to enumerate the tasks to add to a taskpad.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTASK</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTASK</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTASK</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ienumtask-clone">Clone</a>
</td>
<td align="left" width="63%">
Not used by MMC. Creates a new 
<b>IEnumTASK</b> object that has the same state as this 
<b>IEnumTASK</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ienumtask-next">Next</a>
</td>
<td align="left" width="63%">
Enables MMC to retrieve the next task in the snap-in's list of tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ienumtask-reset">Reset</a>
</td>
<td align="left" width="63%">
Enables MMC to reset the enumeration to the beginning of the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-ienumtask-skip">Skip</a>
</td>
<td align="left" width="63%">
Not used by MMC. Skips the specified number of tasks.

</td>
</tr>
</table> 

