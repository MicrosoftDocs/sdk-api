---
UID: NF:msi.MsiCloseAllHandles
title: MsiCloseAllHandles function
author: windows-sdk-content
description: The MsiCloseAllHandles function closes all open installation handles allocated by the current thread. This is a diagnostic function and should not be used for cleanup.
old-location: setup\msicloseallhandles.htm
tech.root: Msi
ms.assetid: 5914e99b-4895-4d12-bb4e-14a377b2eac4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MsiCloseAllHandles, MsiCloseAllHandles function, _msi_msicloseallhandles, msi/MsiCloseAllHandles, setup.msicloseallhandles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiCloseAllHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiCloseAllHandles
: 
---

# MsiCloseAllHandles function


## -description


The 
<b>MsiCloseAllHandles</b> function closes all open installation handles allocated by the current thread. This is a diagnostic function and should not be used for cleanup.


## -parameters






## -returns



This function returns 0 if all handles are closed. Otherwise, the function returns the number of handles open prior to its call.




## -remarks



<b>MsiCloseAllHandles</b> only closes handles allocated by the calling thread, and does not affect handles allocated by other threads, such as the install handle passed to custom actions.

The 
<a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a> function opens a handle to a package and the 
<a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a> function opens a handle to a product. These function are for use with functions that access the product database.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Handle Management Functions</a>
 

 

