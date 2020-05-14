---
UID: NS:setupapi._SP_TROUBLESHOOTER_PARAMS_A
title: SP_TROUBLESHOOTER_PARAMS_A (setupapi.h)
description: An SP_TROUBLESHOOTER_PARAMS structure corresponds to a DIF_TROUBLESHOOTER installation request.helpviewer_keywords: ["*PSP_TROUBLESHOOTER_PARAMS_A","PSP_TROUBLESHOOTER_PARAMS","PSP_TROUBLESHOOTER_PARAMS structure pointer [Device and Driver Installation]","SP_TROUBLESHOOTER_PARAMS","SP_TROUBLESHOOTER_PARAMS structure [Device and Driver Installation]","SP_TROUBLESHOOTER_PARAMS_A","devinst.sp_troubleshooter_params","di-struct_7bddca54-bae0-4d79-82d3-3663f8066f09.xml","setupapi/PSP_TROUBLESHOOTER_PARAMS","setupapi/SP_TROUBLESHOOTER_PARAMS"]
old-location: devinst\sp_troubleshooter_params.htm
tech.root: devinst
ms.assetid: f92e9aa4-ee29-4e69-be05-9c3c916197eb
ms.date: 12/05/2018
ms.keywords: '*PSP_TROUBLESHOOTER_PARAMS_A, PSP_TROUBLESHOOTER_PARAMS, PSP_TROUBLESHOOTER_PARAMS structure pointer [Device and Driver Installation], SP_TROUBLESHOOTER_PARAMS, SP_TROUBLESHOOTER_PARAMS structure [Device and Driver Installation], SP_TROUBLESHOOTER_PARAMS_A, devinst.sp_troubleshooter_params, di-struct_7bddca54-bae0-4d79-82d3-3663f8066f09.xml, setupapi/PSP_TROUBLESHOOTER_PARAMS, setupapi/SP_TROUBLESHOOTER_PARAMS'
f1_keywords:
- setupapi/SP_TROUBLESHOOTER_PARAMS
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- setupapi.h
api_name:
- SP_TROUBLESHOOTER_PARAMS - sp_troubleshooter_params_a
targetos: Windows
req.typenames: SP_TROUBLESHOOTER_PARAMS_A, *PSP_TROUBLESHOOTER_PARAMS_A
req.redist: 
ms.custom: 19H1
---

# SP_TROUBLESHOOTER_PARAMS_A structure


## -description


An SP_TROUBLESHOOTER_PARAMS structure corresponds to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-troubleshooter">DIF_TROUBLESHOOTER</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>. 


### -field ChmFile

Optionally specifies a string buffer that contains the path of a CHM file. The CHM file contains HTML help topics with troubleshooting information. The path must be fully qualified if the file is not in default system help directory (%SystemRoot%\help). 


### -field HtmlTroubleShooter

Optionally specifies a string buffer that contains the path of a topic in the <b>ChmFile</b>. This parameter identifies the page of the <b>ChmFile</b> that Windows should display first.


## -remarks



An installer fills in this structure in response to a DIF_TROUBLESHOOTER request.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-troubleshooter">DIF_TROUBLESHOOTER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>
 

 

