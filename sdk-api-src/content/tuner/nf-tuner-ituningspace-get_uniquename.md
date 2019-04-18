---
UID: NF:tuner.ITuningSpace.get_UniqueName
title: ITuningSpace::get_UniqueName (tuner.h)
author: windows-sdk-content
description: The get_UniqueName method retrieves the unique name of the tuning space.
old-location: mstv\ituningspace_get_uniquename.htm
tech.root: mstv
ms.assetid: 5c605f8c-7b0c-478d-a823-19e2f396953a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_UniqueName method, ITuningSpace.get_UniqueName, ITuningSpace::get_UniqueName, ITuningSpaceget_UniqueName, get_UniqueName, get_UniqueName method [Microsoft TV Technologies], get_UniqueName method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_uniquename, tuner/ITuningSpace::get_UniqueName
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpace.get_UniqueName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpace::get_UniqueName


## -description



The <b>get_UniqueName</b> method retrieves the unique name of the tuning space.




## -parameters




### -param Name [out]

Pointer to a variable that receives the unique name.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

