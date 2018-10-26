---
UID: NN:shobjidl.ICDBurn
title: ICDBurn
author: windows-sdk-content
description: Exposes methods that determine whether a system has hardware for writing to CD, the drive letter of a CD writer device, and programmatically initiate a CD writing session.
old-location: shell\ICDBurn.htm
tech.root: shell
ms.assetid: 8867ae52-2109-4967-b9b9-a4fe89cf4622
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ICDBurn, ICDBurn interface [Windows Shell], ICDBurn interface [Windows Shell],described, _shell_ICDBurn, shell.ICDBurn, shobjidl/ICDBurn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDBurn interface


## -description


Exposes methods that determine whether a system has hardware for writing to CD, the drive letter of a CD writer device, and programmatically initiate a CD writing session.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICDBurn</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICDBurn</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e081973a-e923-45de-93ba-3281be73cc93">Burn</a>
</td>
<td align="left" width="63%">
Instructs data to be copied from the staging area to a writable CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee10152-6823-49bb-836d-3e0cf6c2bb0b">GetRecorderDriveLetter</a>
</td>
<td align="left" width="63%">
Gets the drive letter of a CD drive that has been marked as write-enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b20b5242-2d38-4f86-9267-a2211ef07a00">HasRecordableDrive</a>
</td>
<td align="left" width="63%">
Scans the system for a CD drive with write-capability, returning <b>TRUE</b> if one is found.

</td>
</tr>
</table> 

