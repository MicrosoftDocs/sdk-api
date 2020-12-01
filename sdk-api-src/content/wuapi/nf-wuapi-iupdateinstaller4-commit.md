---
UID: NF:wuapi.IUpdateInstaller4.Commit
title: IUpdateInstaller4::Commit (wuapi.h)
description: Finalizes updates that were previously staged or installed.
helpviewer_keywords: ["Commit","Commit method [Windows Update Agent]","Commit method [Windows Update Agent]","IUpdateInstaller4 interface","IUpdateInstaller4 interface [Windows Update Agent]","Commit method","IUpdateInstaller4.Commit","IUpdateInstaller4::Commit","wua.iupdateinstaller4_commit","wuapi/IUpdateInstaller4::Commit"]
old-location: wua\iupdateinstaller4_commit.htm
tech.root: wua
ms.assetid: F94F443D-9A15-42C3-A404-B80F5E498AD3
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Windows Update Agent], Commit method [Windows Update Agent],IUpdateInstaller4 interface, IUpdateInstaller4 interface [Windows Update Agent],Commit method, IUpdateInstaller4.Commit, IUpdateInstaller4::Commit, wua.iupdateinstaller4_commit, wuapi/IUpdateInstaller4::Commit
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1507 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateInstaller4::Commit
 - wuapi/IUpdateInstaller4::Commit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateInstaller4.Commit
---

# IUpdateInstaller4::Commit


## -description

Finalizes updates that were previously staged or installed.

## -parameters

### -param dwFlags

Reserved for future use.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.

## Remarks
The **Commit** API was made public in the 1809 SDK. Any app compiled with the wuapi.h header can use the **Commit** method on previous versions of Windows 10 as well.

**Commit** should only be called once. This call should happen just prior to commencing a reboot. Calling it multiple times prior to a reboot is not supported and may cause the update to fail.

Calling **Commit** is required prior to rebooting when a feature update is pending reboot. If **Commit** is not called in this circumstance the update won’t be finalized and installed during the reboot.

**Commit** is safe to call prior to reboot for any other types of updates as well.

## -see-also

<a href="/previous-versions/mt694206(v=vs.85)">IUpdateInstaller4</a>