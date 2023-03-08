---
UID: NF:ctffunc.ITfFnConfigure.Show
title: ITfFnConfigure::Show (ctffunc.h)
description: ITfFnConfigure::Show method
helpviewer_keywords: ["ITfFnConfigure interface [Text Services Framework]","Show method","ITfFnConfigure.Show","ITfFnConfigure::Show","Show","Show method [Text Services Framework]","Show method [Text Services Framework]","ITfFnConfigure interface","_tsf_itffnconfigure_show_ref","ctffunc/ITfFnConfigure::Show","tsf.itffnconfigure_show"]
old-location: tsf\itffnconfigure_show.htm
tech.root: TSF
ms.assetid: 34670748-460b-4ece-b742-83b0cf87d901
ms.date: 12/05/2018
ms.keywords: ITfFnConfigure interface [Text Services Framework],Show method, ITfFnConfigure.Show, ITfFnConfigure::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfFnConfigure interface, _tsf_itffnconfigure_show_ref, ctffunc/ITfFnConfigure::Show, tsf.itffnconfigure_show
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - ITfFnConfigure::Show
 - ctffunc/ITfFnConfigure::Show
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
 - ITfFnConfigure.Show
---

# ITfFnConfigure::Show


## -description

Called when the user opens the Text Services control panel application, selects the text service from the list and presses the Properties pushbutton.

## -parameters

### -param hwndParent [in]

Handle of the parent window. The text service typically uses this as the parent or owner window when creating a dialog box.

### -param langid [in]

Contains a <b>LANGID</b> value that specifies the identifier of the language selected in the Text Services control panel application.

### -param rguidProfile [in]

Contains a GUID value that specifies the language profile identifier that the text service is under. This is the value specified in <a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should not return until the user closes the dialog box or property sheet.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnconfigure">ITfFnConfigure</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile">ITfInputProcessorProfiles::AddLanguageProfile
      </a>