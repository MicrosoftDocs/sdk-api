---
UID: NS:setupapi._SP_TROUBLESHOOTER_PARAMS_A
title: "_SP_TROUBLESHOOTER_PARAMS_A"
author: windows-driver-content
description: An SP_TROUBLESHOOTER_PARAMS structure corresponds to a DIF_TROUBLESHOOTER installation request.
old-location: devinst\sp_troubleshooter_params.htm
old-project: devinst
ms.assetid: f92e9aa4-ee29-4e69-be05-9c3c916197eb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSP_TROUBLESHOOTER_PARAMS_A, PSP_TROUBLESHOOTER_PARAMS, PSP_TROUBLESHOOTER_PARAMS structure pointer [Device and Driver Installation], SP_TROUBLESHOOTER_PARAMS, SP_TROUBLESHOOTER_PARAMS structure [Device and Driver Installation], SP_TROUBLESHOOTER_PARAMS_A, _SP_TROUBLESHOOTER_PARAMS_A, devinst.sp_troubleshooter_params, di-struct_7bddca54-bae0-4d79-82d3-3663f8066f09.xml, setupapi/PSP_TROUBLESHOOTER_PARAMS, setupapi/SP_TROUBLESHOOTER_PARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: SP_TROUBLESHOOTER_PARAMS_A, *PSP_TROUBLESHOOTER_PARAMS_A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	setupapi.h
api_name:
-	SP_TROUBLESHOOTER_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SP_TROUBLESHOOTER_PARAMS_A structure


## -description


An SP_TROUBLESHOOTER_PARAMS structure corresponds to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543726">DIF_TROUBLESHOOTER</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>. 


### -field ChmFile

Optionally specifies a string buffer that contains the path of a CHM file. The CHM file contains HTML help topics with troubleshooting information. The path must be fully qualified if the file is not in default system help directory (%SystemRoot%\help). 


### -field HtmlTroubleShooter

Optionally specifies a string buffer that contains the path of a topic in the <b>ChmFile</b>. This parameter identifies the page of the <b>ChmFile</b> that Windows should display first.


## -remarks



An installer fills in this structure in response to a DIF_TROUBLESHOOTER request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543726">DIF_TROUBLESHOOTER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

