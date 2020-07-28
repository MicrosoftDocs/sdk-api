---
UID: NF:dshowasf.IConfigAsfWriter.GetIndexMode
title: IConfigAsfWriter::GetIndexMode (dshowasf.h)
description: The GetIndexMode method retrieves the current index mode.
helpviewer_keywords: ["GetIndexMode","GetIndexMode method [DirectShow]","GetIndexMode method [DirectShow]","IConfigAsfWriter interface","IConfigAsfWriter interface [DirectShow]","GetIndexMode method","IConfigAsfWriter.GetIndexMode","IConfigAsfWriter::GetIndexMode","IConfigAsfWriterGetIndexMode","dshow.iconfigasfwriter_getindexmode","dshowasf/IConfigAsfWriter::GetIndexMode"]
old-location: dshow\iconfigasfwriter_getindexmode.htm
tech.root: dshow
ms.assetid: 70d9a2e7-2f5a-4f87-b42c-3a225c42a44b
ms.date: 12/05/2018
ms.keywords: GetIndexMode, GetIndexMode method [DirectShow], GetIndexMode method [DirectShow],IConfigAsfWriter interface, IConfigAsfWriter interface [DirectShow],GetIndexMode method, IConfigAsfWriter.GetIndexMode, IConfigAsfWriter::GetIndexMode, IConfigAsfWriterGetIndexMode, dshow.iconfigasfwriter_getindexmode, dshowasf/IConfigAsfWriter::GetIndexMode
f1_keywords:
- dshowasf/IConfigAsfWriter.GetIndexMode
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
- IConfigAsfWriter.GetIndexMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Use this method to determine whether the WM ASF Writer is currently configured to write indexed ASF files. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode">IConfigAsfWriter::SetIndexMode</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter">IConfigAsfWriter Interface</a>
 

 

