---
UID: NF:oleacc.GetOleaccVersionInfo
title: GetOleaccVersionInfo function
author: windows-sdk-content
description: Retrieves the version number and build number of the Microsoft Active Accessibility file Oleacc.dll.
old-location: winauto\getoleaccversioninfo.htm
tech.root: WinAuto
ms.assetid: 96dcdb85-4f35-4274-ba57-2f565c3ebb5f
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetOleaccVersionInfo, GetOleaccVersionInfo function [Windows Accessibility], _msaa_GetOleaccVersionInfo, msaa.getoleaccversioninfo, oleacc/GetOleaccVersionInfo, winauto.getoleaccversioninfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - GetOleaccVersionInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# GetOleaccVersionInfo function


## -description


Retrieves the version number and build number of the Microsoft Active Accessibility file Oleacc.dll.


## -parameters




### -param pVer [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Address of a <b>DWORD</b> that receives the version number. The major version number is placed in the high word, and the minor version number is placed in the low word.


### -param pBuild [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Address of a <b>DWORD</b> that receives the build number. The major build number is placed in the high word, and the minor build number is placed in the low word.


## -returns



This function does not return a value.




## -remarks



This function provides an easy way to get the version and build numbers for Oleacc.dll. The <a href="http://go.microsoft.com/fwlink/p/?linkid=178218">GetFileVersionInfoSize</a>, <a href="http://go.microsoft.com/fwlink/p/?linkid=178219">GetFileVersionInfo</a>, and <a href="http://go.microsoft.com/fwlink/p/?linkid=178220">VerQueryValue</a> functions can be used to retrieve the same information.



