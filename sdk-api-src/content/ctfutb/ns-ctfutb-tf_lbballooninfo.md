---
UID: NS:ctfutb.TF_LBBALLOONINFO
title: TF_LBBALLOONINFO (ctfutb.h)
author: windows-sdk-content
description: The TF_LBBALLOONINFO structure contains information about a language bar balloon item.
old-location: tsf\tf_lbballooninfo.htm
tech.root: TSF
ms.assetid: 8ceed1ae-27f9-4998-b950-52865bfa2f79
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TF_LBBALLOONINFO, TF_LBBALLOONINFO structure [Text Services Framework], _tsf_tf_lbballooninfo_ref, ctfutb/TF_LBBALLOONINFO, tsf.tf_lbballooninfo
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: TF_LBBALLOONINFO
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_LBBALLOONINFO structure


## -description



The <b>TF_LBBALLOONINFO</b> structure contains information about a language bar balloon item.




## -struct-fields




### -field style

Contains one of the <a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle</a> values that specify the type of balloon to display.


### -field bstrText

Contains a <b>BSTR</b> that contains the string for the balloon. This string must be allocated using the <a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> function. The caller free this buffer when it is no longer required by calling <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.


## -see-also




<a href="https://msdn.microsoft.com/4cf695dc-dfb7-4541-a364-4395650f9419">ITfLangBarItemBalloon::GetBalloonInfo
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>



<a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle
      </a>
 

 

