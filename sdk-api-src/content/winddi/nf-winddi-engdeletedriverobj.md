---
UID: NF:winddi.EngDeleteDriverObj
title: EngDeleteDriverObj function
author: windows-sdk-content
description: The EngDeleteDriverObj function frees the handle used for tracking a device-managed resource.
old-location: display\engdeletedriverobj.htm
old-project: display
ms.assetid: 5c4f7f6a-331e-4c5d-9663-6a84245a203f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngDeleteDriverObj, EngDeleteDriverObj function [Display Devices], display.engdeletedriverobj, gdifncs_6aada185-b1c4-4b55-9bc0-cc89d0bc67d4.xml, winddi/EngDeleteDriverObj
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngDeleteDriverObj
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteDriverObj function


## -description


The <b>EngDeleteDriverObj</b> function frees the handle used for tracking a device-managed resource.


## -parameters




### -param hdo

Handle to the driver object that is to be deleted. This GDI handle was obtained from <a href="https://msdn.microsoft.com/2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2">EngCreateDriverObj</a>.


### -param bCallBack

Specifies whether the cleanup callback should be called. If <b>TRUE</b>, GDI invokes the cleanup callback before removing the <a href="https://msdn.microsoft.com/313ee1bf-ee0c-4283-b5e1-5bbabb944a4a">DRIVEROBJ</a> from the handle manager. If <b>FALSE</b>, GDI does not do so. If the callback function returns failure, <b>EngDeleteDriverObj</b> will fail.


### -param bLocked

Specifies whether the object was locked by the driver (through a call to <a href="https://msdn.microsoft.com/9ed3142d-2b20-4453-9057-80e6f8f92ff2">EngLockDriverObj</a>) before <b>EngDeleteDriverObj</b> was called. If <b>TRUE</b>, the object was locked; if <b>FALSE</b>, the object was not locked.


## -returns



The return value is <b>TRUE</b> if the function is successful and the handle is freed; it is <b>FALSE</b> if the handle has not been freed. If the <i>pFreeObjProc</i> driver function specified in <b>EngCreateDriverObj</b> returns <b>FALSE</b>, then <b>EngDeleteDriverObj</b> will fail and the handle won't be freed. This could happen if the cleanup callback needs to lock another DRIVEROBJ structure (in order to free the current DRIVEROBJ structure ) and fails because the other DRIVEROBJ structure is in use by another thread.




## -remarks



After the handle is freed, the associated driver resource is no longer tracked by GDI and the function pointed to by the <i>pFreeObjProc</i> parameter of <a href="https://msdn.microsoft.com/2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2">EngCreateDriverObj </a><i>will not</i> be called upon process termination. It is the responsibility of the driver to ensure that the resource is freed.

Most drivers should be consistent in how objects are cleaned up at termination time. Consequently, they will pass <b>TRUE</b> for <i>bCallback</i>, indicating to GDI that it should call the driver's cleanup function to free this driver resource.

The <i>bCallBack</i> parameter indicates to GDI whether the callback function needs to be called. Passing <b>TRUE</b> for <i>bCallBack</i> tells GDI to call the driver's cleanup function back to free this driver resource. Passing <b>FALSE</b> prevents GDI from calling the cleanup function. If <i>pFreeObjProc</i> returns <b>FALSE</b>, <b>EngDeleteDriverObj</b> fails and the handle won't be freed. For example, this could happen if the <i>pFreeObjProc</i> needed to lock down another DRIVEROBJ structure to free the current DRIVEROBJ structure and failed because the structure was being used by another thread. The <i>pFreeObjProc</i> should never fail at cleanup time, because no threads, other than the cleanup thread, are running, so locks of other objects won't fail.

The <i>bLocked</i> parameter indicates to GDI that the object has already been locked once by the driver. Often, before an object is deleted, the driver might have locked it down to use first. This allows the driver to call GDI without first having to unlock the object, thus eliminating the possibility that another thread could enter the driver and lock it down before the handle is freed.




## -see-also




<a href="https://msdn.microsoft.com/313ee1bf-ee0c-4283-b5e1-5bbabb944a4a">DRIVEROBJ</a>



<a href="https://msdn.microsoft.com/2912a456-e5d7-4ae4-b8b0-d16c9e8eadf2">EngCreateDriverObj</a>
 

 

