---
UID: NF:icm.UnregisterCMMW
title: UnregisterCMMW function
author: windows-driver-content
description: The UnregisterCMM function dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).
old-location: wcs\unregistercmm.htm
old-project: WCS
ms.assetid: b965db49-6131-4146-b298-77455b80972d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: UnregisterCMM, UnregisterCMM function [Windows Color System], UnregisterCMMA, UnregisterCMMW, _color_UnregisterCMM, icm/UnregisterCMM, icm/UnregisterCMMA, icm/UnregisterCMMW, wcs.unregistercmm
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
req.unicode-ansi: UnregisterCMMW (Unicode) and UnregisterCMMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	UnregisterCMM
-	UnregisterCMMA
-	UnregisterCMMW
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# UnregisterCMMW function


## -description


The <b>UnregisterCMM</b> function dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).


## -parameters




### -param pMachineName

Reserved; must currently be set to <b>NULL</b>, until non-local registration is supported. This parameter is intended to point to the name of the computer on which a CMM DLLs registration should be removed. A <b>NULL</b> pointer indicates the local computer.


### -param cmmID

Specifies the ID value identifying the CMM whose registration is to be removed. This is the signature of the CMM registered with the International Color Consortium (ICC).


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the profile for creating a transform later specifies this ID, the Windows default CMM will be used rather than this CMM DLL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

