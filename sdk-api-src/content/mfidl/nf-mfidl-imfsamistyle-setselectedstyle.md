---
UID: NF:mfidl.IMFSAMIStyle.SetSelectedStyle
title: IMFSAMIStyle::SetSelectedStyle (mfidl.h)
author: windows-sdk-content
description: Sets the current style on the SAMI media source.
old-location: mf\imfsamistyle_setselectedstyle.htm
tech.root: medfound
ms.assetid: f7179756-517b-400b-8676-fd9ab5bbe74c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSAMIStyle interface [Media Foundation],SetSelectedStyle method, IMFSAMIStyle.SetSelectedStyle, IMFSAMIStyle::SetSelectedStyle, SetSelectedStyle, SetSelectedStyle method [Media Foundation], SetSelectedStyle method [Media Foundation],IMFSAMIStyle interface, f7179756-517b-400b-8676-fd9ab5bbe74c, mf.imfsamistyle_setselectedstyle, mfidl/IMFSAMIStyle::SetSelectedStyle
ms.topic: method
f1_keywords: 
 - "mfidl/IMFSAMIStyle.SetSelectedStyle"
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSAMIStyle.SetSelectedStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSAMIStyle::SetSelectedStyle


## -description


Sets the current style on the SAMI media source.


## -parameters




### -param pwszStyle [in]

Pointer to a null-terminated string containing the name of the style. To clear the current style, pass an empty string ("").  To get the list of style names, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles">IMFSAMIStyle::GetStyles</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle">IMFSAMIStyle</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>
 

 

