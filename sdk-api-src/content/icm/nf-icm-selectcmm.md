---
UID: NF:icm.SelectCMM
title: SelectCMM function
author: windows-sdk-content
description: SelectCMM allows an application to select the preferred color management module (CMM) to use.
old-location: wcs\selectcmm.htm
tech.root: WCS
ms.assetid: 3aadd3d6-a74e-4de2-855c-d20c520821ff
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SelectCMM, SelectCMM function [Windows Color System], _color_SelectCMM, icm/SelectCMM, wcs.selectcmm
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
req.unicode-ansi: 
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
 - SelectCMM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SelectCMM function


## -description


<b>SelectCMM</b> allows an application to select the preferred color management module (CMM) to use.


## -parameters




### -param dwCMMType

TBD




#### - cmmID

Specifies the signature of the desired CMM as registered with the International Color Consortium (ICC). 

<b>Windows 2000 only:</b> Setting this parameter to <b>NULL</b> causes the WCS system to select the default CMM.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



For <b>SelectCMM</b> to succeed, the specified CMM must be registered with the system.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

