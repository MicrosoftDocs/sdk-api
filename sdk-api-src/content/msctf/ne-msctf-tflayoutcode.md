---
UID: NE:msctf.__MIDL_ITfTextLayoutSink_0001
title: TfLayoutCode (msctf.h)
description: Elements of the TfLayoutCode enumeration specify the type of layout change in an ITfTextLayoutSink::OnLayoutChange notification.
helpviewer_keywords: ["TF_LC_CHANGE","TF_LC_CREATE","TF_LC_DESTROY","TfLayoutCode","TfLayoutCode enumeration [Text Services Framework]","_tsf_tflayoutcode_ref","msctf/TF_LC_CHANGE","msctf/TF_LC_CREATE","msctf/TF_LC_DESTROY","msctf/TfLayoutCode","tsf.tflayoutcode"]
old-location: tsf\tflayoutcode.htm
tech.root: TSF
ms.assetid: b9ff6d11-68f2-47c5-b8d7-b3bc2533fdbb
ms.date: 12/05/2018
ms.keywords: TF_LC_CHANGE, TF_LC_CREATE, TF_LC_DESTROY, TfLayoutCode, TfLayoutCode enumeration [Text Services Framework], _tsf_tflayoutcode_ref, msctf/TF_LC_CHANGE, msctf/TF_LC_CREATE, msctf/TF_LC_DESTROY, msctf/TfLayoutCode, tsf.tflayoutcode
f1_keywords:
- msctf/TfLayoutCode
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Msctf.h
api_name:
- TfLayoutCode
targetos: Windows
req.typenames: TfLayoutCode
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# TfLayoutCode enumeration


## -description


Elements of the <b>TfLayoutCode</b> enumeration specify the type of layout change in an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextlayoutsink-onlayoutchange">ITfTextLayoutSink::OnLayoutChange</a> notification.


## -enum-fields




### -field TF_LC_CREATE

The view has just been created.


### -field TF_LC_CHANGE

The view layout has changed.


### -field TF_LC_DESTROY

The view is about to be destroyed.


## -remarks



In TSF, a view is on-screen rendering of document content. These constants are assigned to parameters of methods of the <b>ITf*</b> interfaces, but not those of the <b>IText*</b> interfaces.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itftextlayoutsink-onlayoutchange">ITfTextLayoutSink::OnLayoutChange
      </a>
 

 

