---
UID: NN:imapi.IDiscMaster
title: IDiscMaster (imapi.h)
description: The IDiscMaster interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc.
helpviewer_keywords: ["IDiscMaster","IDiscMaster interface [IMAPI]","IDiscMaster interface [IMAPI]","described","_win32_idiscmaster","base.idiscmaster","imapi.idiscmaster","imapi/IDiscMaster"]
old-location: imapi\idiscmaster.htm
tech.root: imapi
ms.assetid: 1473e79e-a13a-4bc5-b80d-d8921fdc9952
ms.date: 12/05/2018
ms.keywords: IDiscMaster, IDiscMaster interface [IMAPI], IDiscMaster interface [IMAPI],described, _win32_idiscmaster, base.idiscmaster, imapi.idiscmaster, imapi/IDiscMaster
f1_keywords:
- imapi/IDiscMaster
dev_langs:
- c++
req.header: imapi.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Actxprxy.dll
api_name:
- IDiscMaster
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscMaster interface


## -description


The 
<b>IDiscMaster</b> interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc. Although an image mastering object can support several formats, it may not be possible to access all formats through a specific recorder. For this reason, you must select a recorder with 
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a> after selecting a format with 
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMaster</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiscMaster</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscMaster</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-clearformatcontent">ClearFormatContent</a>
</td>
<td align="left" width="63%">
Clears the contents of an unburned image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-close">Close</a>
</td>
<td align="left" width="63%">
Closes the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscmasterformats">EnumDiscMasterFormats</a>
</td>
<td align="left" width="63%">
Retrieves a format enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-enumdiscrecorders">EnumDiscRecorders</a>
</td>
<td align="left" width="63%">
Retrieves a recorder enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-getactivediscmasterformat">GetActiveDiscMasterFormat</a>
</td>
<td align="left" width="63%">
Retrieves the currently selected recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-getactivediscrecorder">GetActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the active disc recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-open">Open</a>
</td>
<td align="left" width="63%">
Opens an IMAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressadvise">ProgressAdvise</a>
</td>
<td align="left" width="63%">
Registers for progress notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-progressunadvise">ProgressUnadvise</a>
</td>
<td align="left" width="63%">
Cancels progress notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">RecordDisc</a>
</td>
<td align="left" width="63%">
Burns the staged image to media in the active disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscmasterformat">SetActiveDiscMasterFormat</a>
</td>
<td align="left" width="63%">
Sets a new active recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Selects a new active disc recorder.

</td>
</tr>
</table> 

