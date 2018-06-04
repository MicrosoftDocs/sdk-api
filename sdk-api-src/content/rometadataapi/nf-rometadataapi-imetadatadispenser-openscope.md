---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMetaDataDispenser::OpenScope


## -description


Opens an existing, on-disk file and maps its metadata into memory.


## -parameters




### -param szScope [in]

The name of the file to be opened. The file must contain common language runtime (CLR) metadata.


### -param dwOpenFlags [in]

Specifies the mode (read, write, and so on) for opening. value of the <a href="http://msdn.microsoft.com/en-us/library/ms233112.aspx">CorOpenFlags</a> enumeration to specify the mode (read, write, and so on) for opening.




### -param riid [in]

The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.


### -param ppIUnk [out]

The pointer to the returned interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.

If the target file does not contain CLR metadata, the <b>OpenScope</b> method will fail.






## -see-also




<a href="https://msdn.microsoft.com/3454193d-9068-4032-ae9e-b3087509b0b8">IMetaDataDispenser</a>
 

 

