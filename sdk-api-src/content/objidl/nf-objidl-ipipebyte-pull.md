---
UID: NF:objidl.IPipeByte.Pull
title: IPipeByte::Pull (objidl.h)
description: The IPipeByte::Pull method (objidl.h) retrieves data of the byte type from the pipe source.
helpviewer_keywords: ["IPipeByte interface [COM]","Pull method","IPipeByte.Pull","IPipeByte::Pull","Pull","Pull method [COM]","Pull method [COM]","IPipeByte interface","_com_ipipebyte_pull","com.ipipebyte_pull","objidlbase/IPipeByte::Pull"]
old-location: com\ipipebyte_pull.htm
tech.root: com
ms.assetid: 07d4d4cd-de41-41bc-af71-ff12affcbbbe
ms.date: 08/12/2022
ms.keywords: IPipeByte interface [COM],Pull method, IPipeByte.Pull, IPipeByte::Pull, Pull, Pull method [COM], Pull method [COM],IPipeByte interface, _com_ipipebyte_pull, com.ipipebyte_pull, objidlbase/IPipeByte::Pull
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPipeByte::Pull
 - objidl/IPipeByte::Pull
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPipeByte.Pull
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

<a href="/windows/desktop/api/objidl/nn-objidl-ipipebyte">IPipeByte</a>
