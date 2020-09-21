---
UID: NN:wsbapp.IWsbApplicationRestoreSupport
title: IWsbApplicationRestoreSupport (wsbapp.h)
description: Defines methods for performing application-specific restore tasks.
helpviewer_keywords: ["IWsbApplicationRestoreSupport","IWsbApplicationRestoreSupport interface [Windows Server Backup]","IWsbApplicationRestoreSupport interface [Windows Server Backup]","described","wsb.iwsbapplicationrestoresupport","wsbapp/IWsbApplicationRestoreSupport"]
old-location: wsb\iwsbapplicationrestoresupport.htm
tech.root: wsb
ms.assetid: 694f9b4d-0ca8-4dbe-829c-6ac18c9aa140
ms.date: 12/05/2018
ms.keywords: IWsbApplicationRestoreSupport, IWsbApplicationRestoreSupport interface [Windows Server Backup], IWsbApplicationRestoreSupport interface [Windows Server Backup],described, wsb.iwsbapplicationrestoresupport, wsbapp/IWsbApplicationRestoreSupport
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWsbApplicationRestoreSupport
 - wsbapp/IWsbApplicationRestoreSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport
---

# IWsbApplicationRestoreSupport interface


## -description

Defines methods for performing application-specific restore tasks.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWsbApplicationRestoreSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWsbApplicationRestoreSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWsbApplicationRestoreSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationrestoresupport-isrollforwardsupported">IsRollForwardSupported</a>
</td>
<td align="left" width="63%">
Reports whether the application supports roll-forward restore.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationrestoresupport-ordercomponents">OrderComponents</a>
</td>
<td align="left" width="63%">
Specifies the order in which application components are to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationrestoresupport-postrestore">PostRestore</a>
</td>
<td align="left" width="63%">
Performs application-specific <a href="/windows/desktop/VSS/vssgloss-p">PostRestore</a> operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/wsbapp/nf-wsbapp-iwsbapplicationrestoresupport-prerestore">PreRestore</a>
</td>
<td align="left" width="63%">
Performs application-specific <a href="/windows/desktop/VSS/vssgloss-p">PreRestore</a> operations.

</td>
</tr>
</table>