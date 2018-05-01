---
UID: NF:objidlbase.IPipeDouble.Pull
title: IPipeDouble::Pull method
author: windows-driver-content
description: Retrieves data of the double integer type from the pipe source.
old-location: com\ipipedouble_pull.htm
old-project: com
ms.assetid: 393e44fa-48fe-4a8d-b337-9b875129a502
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IPipeDouble, IPipeDouble interface [COM], Pull method, IPipeDouble::Pull, Pull method [COM], Pull method [COM], IPipeDouble interface, Pull,IPipeDouble.Pull, _com_ipipedouble_pull, com.ipipedouble_pull, objidlbase/IPipeDouble::Pull
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IPipeDouble.Pull
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPipeDouble::Pull method


## -description


Retrieves data of the double integer type from the pipe source.


## -parameters




### -param buf [out]

A pointer to the memory buffer that receives the data. The buffer must be able to hold at least the number of double integers specified in <i>cRequest</i>.


### -param cRequest [in]

The number of double integers requested.


### -param pcReturned [out]

The actual number of double integers returned.


## -returns



This method returns S_OK to indicate that the data was retrieved successfully.




## -remarks



When the <b>Pull</b> method is called, data is requested from the provider of the pipe. The caller must provide a buffer that will hold at least the number of double integers specified in the <i>cRequest</i> parameter. The proxy will unmarshal the data into the provided buffer and set the number of double integers actually provided in <i>pcReturned</i>. The <i>pcReturned</i> parameter can be less than or equal to <i>cRequest</i>, but it will never be greater. When <i>pcReturned</i> is 0, it indicates that there is no more data.




## -see-also




<a href="https://msdn.microsoft.com/434d0e0e-55a0-4a08-bc63-ebca4b2bdcca">IPipeDouble</a>
 

 

