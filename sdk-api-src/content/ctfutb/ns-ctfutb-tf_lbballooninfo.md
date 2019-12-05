---
UID: NS:ctfutb.TF_LBBALLOONINFO
title: TF_LBBALLOONINFO (ctfutb.h)
description: The TF_LBBALLOONINFO structure contains information about a language bar balloon item.
old-location: tsf\tf_lbballooninfo.htm
tech.root: TSF
ms.assetid: 8ceed1ae-27f9-4998-b950-52865bfa2f79
ms.date: 12/05/2018
ms.keywords: TF_LBBALLOONINFO, TF_LBBALLOONINFO structure [Text Services Framework], _tsf_tf_lbballooninfo_ref, ctfutb/TF_LBBALLOONINFO, tsf.tf_lbballooninfo
ms.topic: struct
f1_keywords:
- ctfutb/TF_LBBALLOONINFO
dev_langs:
- c++
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
- Ctfutb.h
api_name:
- TF_LBBALLOONINFO
targetos: Windows
req.typenames: TF_LBBALLOONINFO
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# TF_LBBALLOONINFO structure


## -description



The <b>TF_LBBALLOONINFO</b> structure contains information about a language bar balloon item.




## -struct-fields




### -field style

Contains one of the <a href="https://docs.microsoft.com/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle</a> values that specify the type of balloon to display.


### -field bstrText

Contains a <b>BSTR</b> that contains the string for the balloon. This string must be allocated using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> function. The caller free this buffer when it is no longer required by calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo">ITfLangBarItemBalloon::GetBalloonInfo
      </a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>



<a href="https://docs.microsoft.com/windows/win32/api/ctfutb/ne-ctfutb-tflbballoonstyle">TfLBBalloonStyle
      </a>
 

 

