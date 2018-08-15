---
UID: NF:objidl.IPipeByte.Pull
title: IPipeByte::Pull
author: windows-sdk-content
description: Retrieves data of the byte type from the pipe source.
old-location: com\ipipebyte_pull.htm
old-project: com
ms.assetid: 07d4d4cd-de41-41bc-af71-ff12affcbbbe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPipeByte interface [COM],Pull method, IPipeByte.Pull, IPipeByte::Pull, Pull, Pull method [COM], Pull method [COM],IPipeByte interface, _com_ipipebyte_pull, com.ipipebyte_pull, objidlbase/IPipeByte::Pull
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.redist: 
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPipeByte.Pull
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPipeByte::Pull


## -description


Retrieves data of the byte type from the pipe source.


## -parameters




### -param buf [out]

A pointer to the memory buffer that receives the data. The buffer must be able to hold at least the number of bytes specified in <i>cRequest</i>.


### -param cRequest [in]

The number of bytes requested.


### -param pcReturned [out]

The actual number of bytes returned.


## -returns



This method returns S_OK to indicate that the data was retrieved successfully.




## -remarks



When the <b>Pull</b> method is called, data is requested from the provider of the pipe. The caller must provide a buffer that will hold at least the number of bytes specified in the <i>cRequest</i> parameter. The proxy will unmarshal the data into the provided buffer and set the number of bytes actually provided in <i>pcReturned</i>. The <i>pcReturned</i> parameter can be less than or equal to <i>cRequest</i>, but it will never be greater. When <i>pcReturned</i> is 0, it indicates that there is no more data.




## -see-also




<a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>
 

 

