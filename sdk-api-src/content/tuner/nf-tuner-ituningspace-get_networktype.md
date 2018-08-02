---
UID: NF:tuner.ITuningSpace.get_NetworkType
title: ITuningSpace::get_NetworkType
author: windows-sdk-content
description: The get_NetworkType method retrieves the network type of the tuning space as a BSTR.
old-location: mstv\ituningspace_get_networktype.htm
old-project: mstv
ms.assetid: f264b6b3-98ae-44bc-8922-ab35c3b7a0d1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_NetworkType method, ITuningSpace.get_NetworkType, ITuningSpace::get_NetworkType, ITuningSpaceget_NetworkType, get_NetworkType, get_NetworkType method [Microsoft TV Technologies], get_NetworkType method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_networktype, tuner/ITuningSpace::get_NetworkType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpace.get_NetworkType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_NetworkType


## -description



The <b>get_NetworkType</b> method retrieves the network type of the tuning space as a <b>BSTR</b>.



This method is intended for Automation clients, because it returns the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="https://msdn.microsoft.com/54cf0c5b-03fb-4419-976c-acc821dfc7e8">ITuningSpace::get__NetworkType</a> method instead, which returns a GUID value


## -parameters




### -param NetworkTypeGuid






#### - pNetworkTypeGuid [out]

Pointer to a variable that receives a string containing the network type GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

