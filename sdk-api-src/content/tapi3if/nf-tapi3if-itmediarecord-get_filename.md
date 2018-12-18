---
UID: NF:tapi3if.ITMediaRecord.get_FileName
title: ITMediaRecord::get_FileName
author: windows-sdk-content
description: The get_FileName method retrieves the name of the file that was used for recording by this terminal.
old-location: tapi3\itmediarecord_get_filename.htm
tech.root: tapi
ms.assetid: fd97665c-ff9e-4621-baf9-7c0b603400c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITMediaRecord interface [TAPI 2.2],get_FileName method, ITMediaRecord.get_FileName, ITMediaRecord::get_FileName, _tapi3_itmediarecord_get_filename, get_FileName, get_FileName method [TAPI 2.2], get_FileName method [TAPI 2.2],ITMediaRecord interface, tapi3.itmediarecord_get_filename, tapi3if/ITMediaRecord::get_FileName
ms.topic: method
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
---

# ITMediaRecord::get_FileName


## -description


The 
<b>get_FileName</b> method retrieves the name of the file that was used for recording by this terminal.


## -parameters




### -param pbstrFileName [out]

The <b>BSTR</b> representation of the file name. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/604b0128-1461-40f2-98fe-801dbb71e005">ITMediaRecord</a>



<a href="https://msdn.microsoft.com/d3f6155d-3989-49d7-8944-da26fd03617a">put_FileName</a>
 

 

