---
UID: NF:bdaiface.IBDA_NameValueService.SetValue
title: IBDA_NameValueService::SetValue (bdaiface.h)
description: Sets a name/value pair in device memory.helpviewer_keywords: ["IBDA_NameValueService interface [Microsoft TV Technologies]","SetValue method","IBDA_NameValueService.SetValue","IBDA_NameValueService::SetValue","SetValue","SetValue method [Microsoft TV Technologies]","SetValue method [Microsoft TV Technologies]","IBDA_NameValueService interface","bdaiface/IBDA_NameValueService::SetValue","mstv.ibda_namevalueservice_setvalue"]
old-location: mstv\ibda_namevalueservice_setvalue.htm
tech.root: mstv
ms.assetid: 6017658a-b4ce-496a-bf30-b7473f5d43c1
ms.date: 12/05/2018
ms.keywords: IBDA_NameValueService interface [Microsoft TV Technologies],SetValue method, IBDA_NameValueService.SetValue, IBDA_NameValueService::SetValue, SetValue, SetValue method [Microsoft TV Technologies], SetValue method [Microsoft TV Technologies],IBDA_NameValueService interface, bdaiface/IBDA_NameValueService::SetValue, mstv.ibda_namevalueservice_setvalue
f1_keywords:
- bdaiface/IBDA_NameValueService.SetValue
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
- bdaiface.h
api_name:
- IBDA_NameValueService.SetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_NameValueService::SetValue


## -description


Sets a name/value pair in device memory.


## -parameters




### -param ulDialogRequest [in]

Specifies a logical link with a user interface (MMI) dialog box that might be triggered by setting the value. 


### -param bstrLanguage [in]

The language of the dialog box. This string contains an ISO 639-2 language code with a dash followed by an ISO 3166 country/region code.


### -param bstrName [in]

The name of the name/value pair to set.


### -param bstrValue [in]

The value to set.


### -param ulReserved [in]

Reserved. Set to zero.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_namevalueservice">IBDA_NameValueService</a>
 

 

