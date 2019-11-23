---
UID: NN:shobjidl.ICDBurn
title: ICDBurn (shobjidl.h)

description: Exposes methods that determine whether a system has hardware for writing to CD, the drive letter of a CD writer device, and programmatically initiate a CD writing session.
old-location: shell\ICDBurn.htm
tech.root: shell
ms.assetid: 8867ae52-2109-4967-b9b9-a4fe89cf4622

ms.date: 12/05/2018
ms.keywords: ICDBurn, ICDBurn interface [Windows Shell], ICDBurn interface [Windows Shell],described, _shell_ICDBurn, shell.ICDBurn, shobjidl/ICDBurn
ms.topic: interface
f1_keywords: 
 - "shobjidl/ICDBurn"
dev_langs:
 - c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICDBurn
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDBurn interface


## -description


Exposes methods that determine whether a system has hardware for writing to CD, the drive letter of a CD writer device, and programmatically initiate a CD writing session.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICDBurn</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICDBurn</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICDBurn</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icdburn-burn">Burn</a>
</td>
<td align="left" width="63%">
Instructs data to be copied from the staging area to a writable CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icdburn-getrecorderdriveletter">GetRecorderDriveLetter</a>
</td>
<td align="left" width="63%">
Gets the drive letter of a CD drive that has been marked as write-enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-icdburn-hasrecordabledrive">HasRecordableDrive</a>
</td>
<td align="left" width="63%">
Scans the system for a CD drive with write-capability, returning <b>TRUE</b> if one is found.

</td>
</tr>
</table> 

