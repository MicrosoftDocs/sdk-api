---
UID: NF:oledlg.IOleUIObjInfoW.ConvertObject
title: IOleUIObjInfoW::ConvertObject (oledlg.h)
description: Converts the object to the type of the specified CLSID. (Unicode)
helpviewer_keywords: ["ConvertObject","ConvertObject method [COM]","ConvertObject method [COM]","IOleUIObjInfo interface","ConvertObject method [COM]","IOleUIObjInfoA interface","ConvertObject method [COM]","IOleUIObjInfoW interface","IOleUIObjInfo interface [COM]","ConvertObject method","IOleUIObjInfo::ConvertObject","IOleUIObjInfoA interface [COM]","ConvertObject method","IOleUIObjInfoA::ConvertObject","IOleUIObjInfoW interface [COM]","ConvertObject method","IOleUIObjInfoW.ConvertObject","IOleUIObjInfoW::ConvertObject","_ole_IOleUIObjInfo_ConvertObject","com.ioleuiobjinfo_convertobject","oledlg/IOleUIObjInfo::ConvertObject","oledlg/IOleUIObjInfoA::ConvertObject","oledlg/IOleUIObjInfoW::ConvertObject"]
old-location: com\ioleuiobjinfo_convertobject.htm
tech.root: com
ms.assetid: 44611ed3-35de-4b20-adae-d3a28aa11944
ms.date: 12/05/2018
ms.keywords: ConvertObject, ConvertObject method [COM], ConvertObject method [COM],IOleUIObjInfo interface, ConvertObject method [COM],IOleUIObjInfoA interface, ConvertObject method [COM],IOleUIObjInfoW interface, IOleUIObjInfo interface [COM],ConvertObject method, IOleUIObjInfo::ConvertObject, IOleUIObjInfoA interface [COM],ConvertObject method, IOleUIObjInfoA::ConvertObject, IOleUIObjInfoW interface [COM],ConvertObject method, IOleUIObjInfoW.ConvertObject, IOleUIObjInfoW::ConvertObject, _ole_IOleUIObjInfo_ConvertObject, com.ioleuiobjinfo_convertobject, oledlg/IOleUIObjInfo::ConvertObject, oledlg/IOleUIObjInfoA::ConvertObject, oledlg/IOleUIObjInfoW::ConvertObject
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleUIObjInfoW::ConvertObject
 - oledlg/IOleUIObjInfoW::ConvertObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleDlg.h
api_name:
 - IOleUIObjInfo.ConvertObject
 - IOleUIObjInfoW.ConvertObject
 - IOleUIObjInfoA.ConvertObject
---

# IOleUIObjInfoW::ConvertObject


## -description

Converts the object to the type of the specified CLSID.

## -parameters

### -param dwObject [in]

A unique identifier for the object.

### -param clsidNew [in]

The CLSID.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Insufficient access permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>IOleUIObjInfo::ConvertObject</b> needs to convert the object to the CLSID specified. The actions taken by the convert operation are similar to the actions taken after calling <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a>.

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuiobjinfoa">IOleUIObjInfo</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a>
