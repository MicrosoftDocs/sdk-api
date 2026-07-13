---
UID: NF:tapi3if.ITMediaRecord.put_FileName
title: ITMediaRecord::put_FileName (tapi3if.h)
description: The put_FileName method sets the name of the file to record.
helpviewer_keywords: ["ITMediaRecord interface [TAPI 2.2]","put_FileName method","ITMediaRecord.put_FileName","ITMediaRecord::put_FileName","_tapi3_itmediarecord_put_filename","put_FileName","put_FileName method [TAPI 2.2]","put_FileName method [TAPI 2.2]","ITMediaRecord interface","tapi3.itmediarecord_put_filename","tapi3if/ITMediaRecord::put_FileName"]
old-location: tapi3\itmediarecord_put_filename.htm
tech.root: tapi3
ms.assetid: d3f6155d-3989-49d7-8944-da26fd03617a
ms.date: 12/05/2018
ms.keywords: ITMediaRecord interface [TAPI 2.2],put_FileName method, ITMediaRecord.put_FileName, ITMediaRecord::put_FileName, _tapi3_itmediarecord_put_filename, put_FileName, put_FileName method [TAPI 2.2], put_FileName method [TAPI 2.2],ITMediaRecord interface, tapi3.itmediarecord_put_filename, tapi3if/ITMediaRecord::put_FileName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITMediaRecord::put_FileName
 - tapi3if/ITMediaRecord::put_FileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaRecord.put_FileName
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord">ITMediaRecord</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itmediarecord-get_filename">get_FileName</a>