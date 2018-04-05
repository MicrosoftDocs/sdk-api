---
UID: NF:mfidl.IMFSAMIStyle.SetSelectedStyle
title: IMFSAMIStyle::SetSelectedStyle method
author: windows-driver-content
description: Sets the current style on the SAMI media source.
old-location: mf\imfsamistyle_setselectedstyle.htm
old-project: medfound
ms.assetid: f7179756-517b-400b-8676-fd9ab5bbe74c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], SetSelectedStyle method, IMFSAMIStyle::SetSelectedStyle, SetSelectedStyle method [Media Foundation], SetSelectedStyle method [Media Foundation], IMFSAMIStyle interface, SetSelectedStyle,IMFSAMIStyle.SetSelectedStyle, f7179756-517b-400b-8676-fd9ab5bbe74c, mf.imfsamistyle_setselectedstyle, mfidl/IMFSAMIStyle::SetSelectedStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFSAMIStyle.SetSelectedStyle
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSAMIStyle::SetSelectedStyle method


## -description



          Sets the current style on the SAMI media source.


## -parameters




### -param pwszStyle [in]

Pointer to a null-terminated string containing the name of the style. To clear the current style, pass an empty string ("").  To get the list of style names, call <a href="https://msdn.microsoft.com/e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5">IMFSAMIStyle::GetStyles</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4887c52-57af-4783-b853-11fe6ad3510e">IMFSAMIStyle</a>



<a href="https://msdn.microsoft.com/007c8181-089e-4e56-a31d-9d1942f90b07">SAMI Media Source</a>
 

 

