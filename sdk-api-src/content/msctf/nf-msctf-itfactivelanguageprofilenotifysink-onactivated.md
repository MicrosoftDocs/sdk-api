---
UID: NF:msctf.ITfActiveLanguageProfileNotifySink.OnActivated
title: ITfActiveLanguageProfileNotifySink::OnActivated (msctf.h)
description: ITfActiveLanguageProfileNotifySink::OnActivated method
helpviewer_keywords: ["ITfActiveLanguageProfileNotifySink interface [Text Services Framework]","OnActivated method","ITfActiveLanguageProfileNotifySink.OnActivated","ITfActiveLanguageProfileNotifySink::OnActivated","OnActivated","OnActivated method [Text Services Framework]","OnActivated method [Text Services Framework]","ITfActiveLanguageProfileNotifySink interface","_tsf_itfactivelanguageprofilenotifysink_onactivated_ref","msctf/ITfActiveLanguageProfileNotifySink::OnActivated","tsf.itfactivelanguageprofilenotifysink_onactivated"]
old-location: tsf\itfactivelanguageprofilenotifysink_onactivated.htm
tech.root: TSF
ms.assetid: 89444189-254e-4a3c-9c8e-79c8b96aee34
ms.date: 12/05/2018
ms.keywords: ITfActiveLanguageProfileNotifySink interface [Text Services Framework],OnActivated method, ITfActiveLanguageProfileNotifySink.OnActivated, ITfActiveLanguageProfileNotifySink::OnActivated, OnActivated, OnActivated method [Text Services Framework], OnActivated method [Text Services Framework],ITfActiveLanguageProfileNotifySink interface, _tsf_itfactivelanguageprofilenotifysink_onactivated_ref, msctf/ITfActiveLanguageProfileNotifySink::OnActivated, tsf.itfactivelanguageprofilenotifysink_onactivated
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Imekrcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfActiveLanguageProfileNotifySink::OnActivated
 - msctf/ITfActiveLanguageProfileNotifySink::OnActivated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfActiveLanguageProfileNotifySink.OnActivated
---

# ITfActiveLanguageProfileNotifySink::OnActivated


## -description

Called when the active language or text service changes.

## -parameters

Called when the active language or text service changes.

### -param clsid [in]

CLSID of the TSF text service activated or deactivated. This will be **NULL** for a language change.

### -param guidProfile [in]

Profile GUID for the TSF text service. This is specified by the TSF text service when it is installed. This will be <b>NULL</b> for a language change.

### -param fActivated [in]

TRUE if the TSF text service is activated or FALSE if the TSF text service is deactivated.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

[ITfActiveLanguageProfileNotifySink interface](nn-msctf-itfactivelanguageprofilenotifysink.md)

