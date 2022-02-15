---
UID: NF:msi.MsiCloseAllHandles
title: MsiCloseAllHandles function (msi.h)
description: The MsiCloseAllHandles function closes all open installation handles allocated by the current thread. This is a diagnostic function and should not be used for cleanup.
helpviewer_keywords: ["MsiCloseAllHandles","MsiCloseAllHandles function","_msi_msicloseallhandles","msi/MsiCloseAllHandles","setup.msicloseallhandles"]
old-location: setup\msicloseallhandles.htm
tech.root: setup
ms.assetid: 5914e99b-4895-4d12-bb4e-14a377b2eac4
ms.date: 12/05/2018
ms.keywords: MsiCloseAllHandles, MsiCloseAllHandles function, _msi_msicloseallhandles, msi/MsiCloseAllHandles, setup.msicloseallhandles
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiCloseAllHandles
 - msi/MsiCloseAllHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiCloseAllHandles
---

# MsiCloseAllHandles function


## -description

The 
<b>MsiCloseAllHandles</b> function closes all open installation handles allocated by the current thread. This is a diagnostic function and should not be used for cleanup.



## -returns

This function returns 0 if all handles are closed. Otherwise, the function returns the number of handles open prior to its call.

## -remarks

<b>MsiCloseAllHandles</b> only closes handles allocated by the calling thread, and does not affect handles allocated by other threads, such as the install handle passed to custom actions.

The 
<a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a> function opens a handle to a package and the 
<a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a> function opens a handle to a product. These function are for use with functions that access the product database.

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Handle Management Functions</a>
