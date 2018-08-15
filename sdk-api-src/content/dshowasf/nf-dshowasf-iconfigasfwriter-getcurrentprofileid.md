---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfileId
title: IConfigAsfWriter::GetCurrentProfileId
author: windows-sdk-content
description: The GetCurrentProfileId method retrieves the identifier of the WM ASF Writer filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.).
old-location: dshow\iconfigasfwriter_getcurrentprofileid.htm
old-project: DirectShow
ms.assetid: 37288625-368f-41d4-bfdc-bb2fd144f455
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetCurrentProfileId, GetCurrentProfileId method [DirectShow], GetCurrentProfileId method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfileId method, IConfigAsfWriter.GetCurrentProfileId, IConfigAsfWriter::GetCurrentProfileId, IConfigAsfWriterGetCurrentProfileId, dshow.iconfigasfwriter_getcurrentprofileid, dshowasf/IConfigAsfWriter::GetCurrentProfileId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.redist: 
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
 - IConfigAsfWriter.GetCurrentProfileId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IConfigAsfWriter::GetCurrentProfileId


## -description



The <code>GetCurrentProfileId</code> method retrieves the identifier of the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.)




## -parameters




### -param pdwProfileId [out]

Receives the current profile ID.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



This method is obsolete because it applies only to version 4.0 Windows Media Format SDK profiles. Applications should call <a href="https://msdn.microsoft.com/1fa9fc3f-f8fd-42c9-9de2-22717cbb7e91">IConfigAsfWriter::GetCurrentProfile</a> to get the current profile.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter Interface</a>
 

 

