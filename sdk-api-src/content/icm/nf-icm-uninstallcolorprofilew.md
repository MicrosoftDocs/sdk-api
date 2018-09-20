---
UID: NF:icm.UninstallColorProfileW
title: UninstallColorProfileW function
author: windows-sdk-content
description: UninstallColorProfile removes a specified color profile from a specified computer. Associated files are optionally deleted from the system.
old-location: wcs\uninstallcolorprofile.htm
tech.root: WCS
ms.assetid: 2c5a2055-9f5f-4e21-bcbb-a9aa50105598
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UninstallColorProfile, UninstallColorProfile function [Windows Color System], UninstallColorProfileA, UninstallColorProfileW, _color_UninstallColorProfile, icm/UninstallColorProfile, icm/UninstallColorProfileA, icm/UninstallColorProfileW, wcs.uninstallcolorprofile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UninstallColorProfileW (Unicode) and UninstallColorProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - UninstallColorProfile
 - UninstallColorProfileA
 - UninstallColorProfileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UninstallColorProfileW function


## -description


<b>UninstallColorProfile</b> removes a specified color profile from a specified computer. Associated files are optionally deleted from the system.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the machine from which to uninstall the specified profile. A <b>NULL</b> pointer indicates the local machine.


### -param pProfileName

Points to the file name of the profile to uninstall.


### -param bDelete

If set to <b>TRUE</b>, the function deletes the profile from the COLOR directory. If set to <b>FALSE</b>, this function has no effect.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

