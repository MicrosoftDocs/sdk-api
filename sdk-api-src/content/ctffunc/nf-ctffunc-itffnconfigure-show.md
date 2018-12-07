---
UID: NF:ctffunc.ITfFnConfigure.Show
title: ITfFnConfigure::Show
author: windows-sdk-content
description: ITfFnConfigure::Show method
old-location: tsf\itffnconfigure_show.htm
tech.root: TSF
ms.assetid: 34670748-460b-4ece-b742-83b0cf87d901
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfFnConfigure interface [Text Services Framework],Show method, ITfFnConfigure.Show, ITfFnConfigure::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfFnConfigure interface, _tsf_itffnconfigure_show_ref, ctffunc/ITfFnConfigure::Show, tsf.itffnconfigure_show
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfFnConfigure.Show
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnConfigure::Show


## -description




## -parameters




### -param hwndParent [in]

Handle of the parent window. The text service typically uses this as the parent or owner window when creating a dialog box.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the identifier of the language selected in the Text Services control panel application.


### -param rguidProfile [in]

Contains a GUID value that specifies the language profile identifier that the text service is under. This is the value specified in <a href="https://msdn.microsoft.com/en-us/library/ms628545(v=VS.85).aspx">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should not return until the user closes the dialog box or property sheet.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538925(v=VS.85).aspx">ITfFnConfigure</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
 

 

