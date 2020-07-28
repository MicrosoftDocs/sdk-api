---
UID: NF:objidl.IPipeDouble.Pull
title: IPipeDouble::Pull (objidl.h)
description: Retrieves data of the double integer type from the pipe source.
helpviewer_keywords: ["IPipeDouble interface [COM]","Pull method","IPipeDouble.Pull","IPipeDouble::Pull","Pull","Pull method [COM]","Pull method [COM]","IPipeDouble interface","_com_ipipedouble_pull","com.ipipedouble_pull","objidlbase/IPipeDouble::Pull"]
old-location: com\ipipedouble_pull.htm
tech.root: com
ms.assetid: 393e44fa-48fe-4a8d-b337-9b875129a502
ms.date: 12/05/2018
ms.keywords: IPipeDouble interface [COM],Pull method, IPipeDouble.Pull, IPipeDouble::Pull, Pull, Pull method [COM], Pull method [COM],IPipeDouble interface, _com_ipipedouble_pull, com.ipipedouble_pull, objidlbase/IPipeDouble::Pull
f1_keywords:
- objidl/IPipeDouble.Pull
dev_langs:
- c++
req.header: objidl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IPipeDouble.Pull
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPipeDouble::Pull


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




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipipedouble">IPipeDouble</a>
 

 

