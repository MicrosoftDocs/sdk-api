---
UID: NF:dshowasf.IConfigAsfWriter.GetCurrentProfileId
title: IConfigAsfWriter::GetCurrentProfileId (dshowasf.h)
description: The GetCurrentProfileId method retrieves the identifier of the WM ASF Writer filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.).
helpviewer_keywords: ["GetCurrentProfileId","GetCurrentProfileId method [DirectShow]","GetCurrentProfileId method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","GetCurrentProfileId method","IConfigAsfWriter.GetCurrentProfileId","IConfigAsfWriter::GetCurrentProfileId","IConfigAsfWriterGetCurrentProfileId","dshow.iconfigasfwriter_getcurrentprofileid","dshowasf/IConfigAsfWriter::GetCurrentProfileId"]
old-location: dshow\iconfigasfwriter_getcurrentprofileid.htm
tech.root: dshow
ms.assetid: 37288625-368f-41d4-bfdc-bb2fd144f455
ms.date: 12/05/2018
ms.keywords: GetCurrentProfileId, GetCurrentProfileId method [DirectShow], GetCurrentProfileId method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetCurrentProfileId method, IConfigAsfWriter.GetCurrentProfileId, IConfigAsfWriter::GetCurrentProfileId, IConfigAsfWriterGetCurrentProfileId, dshow.iconfigasfwriter_getcurrentprofileid, dshowasf/IConfigAsfWriter::GetCurrentProfileId
f1_keywords:
- dshowasf/IConfigAsfWriter.GetCurrentProfileId
dev_langs:
- c++
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
- IConfigAsfWriter.GetCurrentProfileId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConfigAsfWriter::GetCurrentProfileId


## -description



The <code>GetCurrentProfileId</code> method retrieves the identifier of the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wm-asf-writer-filter">WM ASF Writer</a> filter's profile, only when the filter is using a Windows Media Format 4.0 profile. (Deprecated.)




## -parameters




### -param pdwProfileId [out]

Receives the current profile ID.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



This method is obsolete because it applies only to version 4.0 Windows Media Format SDK profiles. Applications should call <a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-getcurrentprofile">IConfigAsfWriter::GetCurrentProfile</a> to get the current profile.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>
 

 

