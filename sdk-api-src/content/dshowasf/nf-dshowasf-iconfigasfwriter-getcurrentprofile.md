---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfile
title: IConfigAsfWriter::GetCurrentProfile
author: windows-sdk-content
description: The GetCurrentProfile method retrieves the current ASF profile from the WM ASF Writer filter.
old-location: dshow\iconfigasfwriter_getcurrentprofile.htm
old-project: DirectShow
ms.assetid: 1fa9fc3f-f8fd-42c9-9de2-22717cbb7e91
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetCurrentProfile, GetCurrentProfile method [DirectShow], GetCurrentProfile method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfile method, IConfigAsfWriter.GetCurrentProfile, IConfigAsfWriter::GetCurrentProfile, IConfigAsfWriterGetCurrentProfile, dshow.iconfigasfwriter_getcurrentprofile, dshowasf/IConfigAsfWriter::GetCurrentProfile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter.GetCurrentProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IConfigAsfWriter::GetCurrentProfile


## -description



The <code>GetCurrentProfile</code> method retrieves the current ASF profile from the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter.




## -parameters




### -param ppProfile [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface of the profile. The caller must release the interface.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

