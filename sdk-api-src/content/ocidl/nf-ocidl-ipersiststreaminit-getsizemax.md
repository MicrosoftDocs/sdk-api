---
UID: NF:ocidl.IPersistStreamInit.GetSizeMax
title: IPersistStreamInit::GetSizeMax
author: windows-sdk-content
description: Retrieves the size of the stream needed to save the object.
old-location: com\ipersiststreaminit_getsizemax.htm
old-project: com
ms.assetid: 8413eeda-3867-4352-aefb-82579a4861f2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSizeMax, GetSizeMax method [COM], GetSizeMax method [COM],IPersistStreamInit interface, IPersistStreamInit interface [COM],GetSizeMax method, IPersistStreamInit.GetSizeMax, IPersistStreamInit::GetSizeMax, _com_ipersiststreaminit_getsizemax, com.ipersiststreaminit_getsizemax, ocidl/IPersistStreamInit::GetSizeMax
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPersistStreamInit.GetSizeMax
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPersistStreamInit::GetSizeMax


## -description


Retrieves the size of the stream needed to save the object.


## -parameters




### -param pCbSize [out]

The size in bytes of the stream needed to save this object, in bytes.


## -returns



This method returns S_OK to indicate that the size was retrieved successfully.




## -remarks



This method returns the size needed to save an object. You can call this method to determine the size and set the necessary buffers before calling the <a href="https://msdn.microsoft.com/f88b61d0-dd85-4e8e-b445-dfced6521981">IPersistStreamInit::Save</a> method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The <b>GetSizeMax</b> implementation should return a conservative estimate of the necessary size because the caller might call the <a href="https://msdn.microsoft.com/f88b61d0-dd85-4e8e-b445-dfced6521981">IPersistStreamInit::Save</a> method with a non-growable stream.




## -see-also




<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

