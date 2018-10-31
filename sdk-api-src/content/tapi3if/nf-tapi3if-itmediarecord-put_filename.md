---
UID: NF:tapi3if.ITMediaRecord.put_FileName
title: ITMediaRecord::put_FileName
author: windows-sdk-content
description: The put_FileName method sets the name of the file to record.
old-location: tapi3\itmediarecord_put_filename.htm
tech.root: tapi
ms.assetid: d3f6155d-3989-49d7-8944-da26fd03617a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITMediaRecord interface [TAPI 2.2],put_FileName method, ITMediaRecord.put_FileName, ITMediaRecord::put_FileName, _tapi3_itmediarecord_put_filename, put_FileName, put_FileName method [TAPI 2.2], put_FileName method [TAPI 2.2],ITMediaRecord interface, tapi3.itmediarecord_put_filename, tapi3if/ITMediaRecord::put_FileName
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITMediaRecord.put_FileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMediaRecord::put_FileName


## -description


The 
<b>put_FileName</b> method sets the name of the file to record.


## -parameters




### -param bstrFileName [in]

The <b>BSTR</b> representation of the file name.


#### - bAppendIfExists [in]

If this flag is set to <b>TRUE</b>, and a file with this name already exists, the new data will be appended to the file. If this flag is set to <b>FALSE</b>, and the file exists, the new data will overwrite the old data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/604b0128-1461-40f2-98fe-801dbb71e005">ITMediaRecord</a>



<a href="https://msdn.microsoft.com/fd97665c-ff9e-4621-baf9-7c0b603400c5">get_FileName</a>
 

 

