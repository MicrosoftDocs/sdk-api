---
UID: NF:tuner.ITuningSpace.put_NetworkType
title: ITuningSpace::put_NetworkType
author: windows-sdk-content
description: The put_NetworkType method specifies the network type of the tuning space as a BSTR.
old-location: mstv\ituningspace_put_networktype.htm
tech.root: mstv
ms.assetid: 6af7062c-41c9-447f-8d92-bd67b8348933
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_NetworkType method, ITuningSpace.put_NetworkType, ITuningSpace::put_NetworkType, ITuningSpaceput_NetworkType, mstv.ituningspace_put_networktype, put_NetworkType, put_NetworkType method [Microsoft TV Technologies], put_NetworkType method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_NetworkType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITuningSpace.put_NetworkType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuningSpace::put_NetworkType


## -description



The <b>put_NetworkType</b> method specifies the network type of the tuning space as a <b>BSTR</b>.



This method is intended for Automation clients, because it specifies the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="https://msdn.microsoft.com/02e4ec53-e527-4cd2-a424-66c2f3fe4e43">ITuningSpace::put__NetworkType</a> method instead, which takes a GUID value.


## -parameters




### -param NetworkTypeGuid [in]

Contains the string representation of the network type GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

