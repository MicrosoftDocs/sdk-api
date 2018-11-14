---
UID: NF:icm.RegisterCMMW
title: RegisterCMMW function
author: windows-sdk-content
description: RegisterCMM associates a specified identification value with the specified color management module dynamic link library (CMM DLL). When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.
old-location: wcs\registercmm.htm
tech.root: WCS
ms.assetid: e26a98be-2165-437d-a197-08e07952d043
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RegisterCMM, RegisterCMM function [Windows Color System], RegisterCMMA, RegisterCMMW, _color_RegisterCMM, icm/RegisterCMM, icm/RegisterCMMA, icm/RegisterCMMW, wcs.registercmm
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
req.unicode-ansi: RegisterCMMW (Unicode) and RegisterCMMA (ANSI)
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
 - RegisterCMM
 - RegisterCMMA
 - RegisterCMMW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RegisterCMMW
: 
---

# RegisterCMMW function


## -description


<b>RegisterCMM</b> associates a specified identification value with the specified color management module dynamic link library (CMM DLL). When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.


## -parameters




### -param pMachineName

Reserved; must currently be set to <b>NULL</b>, until non-local registration is supported. This parameter is intended to point to the name of the machine on which a CMM DLL should be registered. A <b>NULL</b> pointer indicates the local machine.


### -param cmmID

Specifies the ID signature of the CMM registered with the International Color Consortium (ICC).


### -param pCMMdll

Pointer to the fully qualified path name of the CMM DLL.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

