---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfileGuid
title: IConfigAsfWriter::GetCurrentProfileGuid (dshowasf.h)
author: windows-sdk-content
description: The GetCurrentProfileGuid method retrieves the GUID of the WM ASF Writer filter's current system profile, if any. (Deprecated.).
old-location: dshow\iconfigasfwriter_getcurrentprofileguid.htm
tech.root: DirectShow
ms.assetid: 8958f8d3-40ff-44b1-a817-5dca30636306
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentProfileGuid, GetCurrentProfileGuid method [DirectShow], GetCurrentProfileGuid method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfileGuid method, IConfigAsfWriter.GetCurrentProfileGuid, IConfigAsfWriter::GetCurrentProfileGuid, IConfigAsfWriterGetCurrentProfileGuid, dshow.iconfigasfwriter_getcurrentprofileguid, dshowasf/IConfigAsfWriter::GetCurrentProfileGuid
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
 - IConfigAsfWriter.GetCurrentProfileGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAsfWriter::GetCurrentProfileGuid


## -description



The <code>GetCurrentProfileGuid</code> method retrieves the GUID of the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter's current system profile, if any. (Deprecated.)




## -parameters




### -param pProfileGuid [out]

Receives the <b>GUID</b> of the system profile.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



This method applies only when the WM ASF Writer filter is configured with a system profile. If the application provided its own ASF profile instead of a system profile (as is recommended), the profile GUID is GUID_NULL. Applications should call <a href="https://msdn.microsoft.com/en-us/library/Dd312026(v=VS.85).aspx">IConfigAsfWriter::GetCurrentProfile</a> to get the current profile.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd312017(v=VS.85).aspx">IConfigAsfWriter Interface</a>
 

 

