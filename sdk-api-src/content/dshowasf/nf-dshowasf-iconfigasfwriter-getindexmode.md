---
UID: NF:dshowasf.IConfigAsfWriter.GetIndexMode
title: IConfigAsfWriter::GetIndexMode
author: windows-sdk-content
description: The GetIndexMode method retrieves the current index mode.
old-location: dshow\iconfigasfwriter_getindexmode.htm
tech.root: DirectShow
ms.assetid: 70d9a2e7-2f5a-4f87-b42c-3a225c42a44b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetIndexMode, GetIndexMode method [DirectShow], GetIndexMode method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetIndexMode method, IConfigAsfWriter.GetIndexMode, IConfigAsfWriter::GetIndexMode, IConfigAsfWriterGetIndexMode, dshow.iconfigasfwriter_getindexmode, dshowasf/IConfigAsfWriter::GetIndexMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.GetIndexMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter::GetIndexMode


## -description



The <code>GetIndexMode</code> method retrieves the current index mode.




## -parameters




### -param pbIndexFile [out]

Receives the index mode setting. A value of <b>TRUE</b> indicates that the WM ASF Writer is configured to write indexed files.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



Use this method to determine whether the WM ASF Writer is currently configured to write indexed ASF files. For more information, see <a href="https://msdn.microsoft.com/d7f5d13a-d36e-4da2-babc-0446e5697b61">IConfigAsfWriter::SetIndexMode</a>.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

