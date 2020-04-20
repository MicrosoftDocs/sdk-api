---
UID: NF:objidl.IPipeDouble.Push
title: IPipeDouble::Push (objidl.h)
description: Sends data of the double integer type to the pipe source.helpviewer_keywords: ["IPipeDouble interface [COM]","Push method","IPipeDouble.Push","IPipeDouble::Push","Push","Push method [COM]","Push method [COM]","IPipeDouble interface","_com_ipipedouble_push","com.ipipedouble_push","objidlbase/IPipeDouble::Push"]
old-location: com\ipipedouble_push.htm
tech.root: com
ms.assetid: 49c9121f-eb92-42e4-bd30-fe2213d44de9
ms.date: 12/05/2018
ms.keywords: IPipeDouble interface [COM],Push method, IPipeDouble.Push, IPipeDouble::Push, Push, Push method [COM], Push method [COM],IPipeDouble interface, _com_ipipedouble_push, com.ipipedouble_push, objidlbase/IPipeDouble::Push
f1_keywords:
- objidl/IPipeDouble.Push
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
- IPipeDouble.Push
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPipeDouble::Push


## -description


Sends data of the double integer type to the pipe source.


## -parameters




### -param buf [in]

A pointer to the memory buffer that holds the data to be sent.


### -param cSent [in]

The number of double integers in the buffer.


## -returns



This method returns S_OK to indicate that the data was sent successfully.




## -remarks



When the <b>Push</b> method is called, the data is being sent to the provider of the pipe. The caller fills the buffer with the data and then calls <b>Push</b>. The number of double integers being sent is specified in the <i>cSent</i> parameter. The caller is responsible for ensuring that the buffer is valid for the duration of the call.

When the last of the data has been pushed, the caller must do one last push of <i>cSent</i> equal to 0 to indicate that the data transfer is complete.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipipedouble">IPipeDouble</a>
 

 

