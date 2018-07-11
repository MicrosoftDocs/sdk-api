---
UID: NS:ctfutb.TF_LBBALLOONINFO
title: TF_LBBALLOONINFO
author: windows-sdk-content
description: The TF_LBBALLOONINFO structure contains information about a language bar balloon item.
old-location: tsf\tf_lbballooninfo.htm
old-project: TSF
ms.assetid: 8ceed1ae-27f9-4998-b950-52865bfa2f79
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: TF_LBBALLOONINFO, TF_LBBALLOONINFO structure [Text Services Framework], _tsf_tf_lbballooninfo_ref, ctfutb/TF_LBBALLOONINFO, tsf.tf_lbballooninfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_LBBALLOONINFO
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
req.lib: 
req.dll: 
req.irql: 
---

# TF_LBBALLOONINFO structure


## -description



The <b>TF_LBBALLOONINFO</b> structure contains information about a language bar balloon item.




## -struct-fields




### -field style

Contains one of the <a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle</a> values that specify the type of balloon to display.


### -field bstrText

Contains a <b>BSTR</b> that contains the string for the balloon. This string must be allocated using the <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> function. The caller free this buffer when it is no longer required by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.


## -see-also




<a href="https://msdn.microsoft.com/4cf695dc-dfb7-4541-a364-4395650f9419">ITfLangBarItemBalloon::GetBalloonInfo
      </a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>



<a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle
      </a>
 

 

