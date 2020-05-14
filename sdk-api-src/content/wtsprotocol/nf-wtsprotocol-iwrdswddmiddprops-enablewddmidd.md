---
UID: NF:wtsprotocol.IWRdsWddmIddProps.EnableWddmIdd
title: IWRdsWddmIddProps::EnableWddmIdd (wtsprotocol.h)
description: Termsrv uses this method to tell protocol stack which mode it is operating.helpviewer_keywords: ["EnableWddmIdd","EnableWddmIdd method [Remote Desktop Services]","EnableWddmIdd method [Remote Desktop Services]","IWRdsWddmIddProps interface","IWRdsWddmIddProps interface [Remote Desktop Services]","EnableWddmIdd method","IWRdsWddmIddProps.EnableWddmIdd","IWRdsWddmIddProps::EnableWddmIdd","termserv.iwrdswddmiddprops_enablewddmidd","wtsprotocol/IWRdsWddmIddProps::EnableWddmIdd"]
old-location: termserv\iwrdswddmiddprops_enablewddmidd.htm
tech.root: TermServ
ms.assetid: 19F07236-6F9C-49F0-B100-E02F9DBF54F7
ms.date: 12/05/2018
ms.keywords: EnableWddmIdd, EnableWddmIdd method [Remote Desktop Services], EnableWddmIdd method [Remote Desktop Services],IWRdsWddmIddProps interface, IWRdsWddmIddProps interface [Remote Desktop Services],EnableWddmIdd method, IWRdsWddmIddProps.EnableWddmIdd, IWRdsWddmIddProps::EnableWddmIdd, termserv.iwrdswddmiddprops_enablewddmidd, wtsprotocol/IWRdsWddmIddProps::EnableWddmIdd
f1_keywords:
- wtsprotocol/IWRdsWddmIddProps.EnableWddmIdd
dev_langs:
- c++
req.header: wtsprotocol.h
req.include-header: 
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
- COM
api_location:
- Wtsprotocol.h
api_name:
- IWRdsWddmIddProps.EnableWddmIdd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsWddmIddProps::EnableWddmIdd


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Termsrv uses this method to tell protocol stack  which mode it is 
    operating.



## -parameters




### -param Enabled [in]

Boolean flag that instructs protocol stack that termsrv supports WDDM IDD mode.


## -returns



S_OK or error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt832805(v=VS.85).aspx">IWRdsWddmIddProps</a>
 

 

