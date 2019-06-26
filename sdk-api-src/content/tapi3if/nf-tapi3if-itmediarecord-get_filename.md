---
UID: NF:tapi3if.ITMediaRecord.get_FileName
title: ITMediaRecord::get_FileName (tapi3if.h)
author: windows-sdk-content
description: The get_FileName method retrieves the name of the file that was used for recording by this terminal.
old-location: tapi3\itmediarecord_get_filename.htm
tech.root: Tapi
ms.assetid: fd97665c-ff9e-4621-baf9-7c0b603400c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITMediaRecord interface [TAPI 2.2],get_FileName method, ITMediaRecord.get_FileName, ITMediaRecord::get_FileName, _tapi3_itmediarecord_get_filename, get_FileName, get_FileName method [TAPI 2.2], get_FileName method [TAPI 2.2],ITMediaRecord interface, tapi3.itmediarecord_get_filename, tapi3if/ITMediaRecord::get_FileName
ms.topic: method
f1_keywords: 
 - "tapi3if/ITMediaRecord.get_FileName"
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaRecord.get_FileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITMediaRecord::get_FileName


## -description


The 
<b>get_FileName</b> method retrieves the name of the file that was used for recording by this terminal.


## -parameters




### -param pbstrFileName [out]

The <b>BSTR</b> representation of the file name. The <b>BSTR</b> is allocated using 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord">ITMediaRecord</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itmediarecord-put_filename">put_FileName</a>
 

 

