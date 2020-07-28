---
UID: NF:bdaiface.IBDA_ConditionalAccess.get_SmartCardApplications
title: IBDA_ConditionalAccess::get_SmartCardApplications (bdaiface.h)
description: The get_SmartCardApplications method retrieves a list of the smart card applications.
helpviewer_keywords: ["IBDA_ConditionalAccess interface [Microsoft TV Technologies]","get_SmartCardApplications method","IBDA_ConditionalAccess.get_SmartCardApplications","IBDA_ConditionalAccess::get_SmartCardApplications","IBDA_ConditionalAccessget_SmartCardApplications","bdaiface/IBDA_ConditionalAccess::get_SmartCardApplications","get_SmartCardApplications","get_SmartCardApplications method [Microsoft TV Technologies]","get_SmartCardApplications method [Microsoft TV Technologies]","IBDA_ConditionalAccess interface","mstv.ibda_conditionalaccess_get_smartcardapplications"]
old-location: mstv\ibda_conditionalaccess_get_smartcardapplications.htm
tech.root: mstv
ms.assetid: 5667ca9c-c46d-43d6-a7da-1f0ff340e869
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccess interface [Microsoft TV Technologies],get_SmartCardApplications method, IBDA_ConditionalAccess.get_SmartCardApplications, IBDA_ConditionalAccess::get_SmartCardApplications, IBDA_ConditionalAccessget_SmartCardApplications, bdaiface/IBDA_ConditionalAccess::get_SmartCardApplications, get_SmartCardApplications, get_SmartCardApplications method [Microsoft TV Technologies], get_SmartCardApplications method [Microsoft TV Technologies],IBDA_ConditionalAccess interface, mstv.ibda_conditionalaccess_get_smartcardapplications
f1_keywords:
- bdaiface/IBDA_ConditionalAccess.get_SmartCardApplications
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
- Bdaiface.h
api_name:
- IBDA_ConditionalAccess.get_SmartCardApplications
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_ConditionalAccess::get_SmartCardApplications


## -description


The <b>get_SmartCardApplications</b> method retrieves a list of the smart card applications.


## -parameters




### -param pulcApplications [in, out]

Receives a count of the number of smart card applications in the <i>rgApplications</i> array.
          


### -param ulcApplicationsMax [in]

The maximum number of smart card applications that the <i>rgApplications</i> buffer can hold.
          


### -param rgApplications [in, out]

Pointer to a buffer that receives an array of smart card applications. Each array element is a <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/ns-bdaiface-smartcardapplication">SmartCardApplication</a> structure.
          


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<div class="alert"><b>Note</b>  The <i>pulcApplications</i> parameter is marked in the IDL file as [in, out] but is used as an [in] parameter. To preserve binary compatibility with previous versions, it has not been changed.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_conditionalaccess">IBDA_ConditionalAccess Interface</a>
 

 

