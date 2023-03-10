---
UID: NF:uiribbon.IUIRibbon.SaveSettingsToStream
title: IUIRibbon::SaveSettingsToStream (uiribbon.h)
description: Writes ribbon settings to a binary stream.
helpviewer_keywords: ["IUIRibbon interface [Windows Ribbon]","SaveSettingsToStream method","IUIRibbon.SaveSettingsToStream","IUIRibbon::SaveSettingsToStream","SaveSettingsToStream","SaveSettingsToStream method [Windows Ribbon]","SaveSettingsToStream method [Windows Ribbon]","IUIRibbon interface","scenicintent_IUIRibbon_SaveSettingsToStream","uiribbon/IUIRibbon::SaveSettingsToStream","windowsribbon.windowsribbon_iuiribbon_savesettingstostream"]
old-location: windowsribbon\windowsribbon_iuiribbon_savesettingstostream.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\savesettingstostream.htm
ms.date: 12/05/2018
ms.keywords: IUIRibbon interface [Windows Ribbon],SaveSettingsToStream method, IUIRibbon.SaveSettingsToStream, IUIRibbon::SaveSettingsToStream, SaveSettingsToStream, SaveSettingsToStream method [Windows Ribbon], SaveSettingsToStream method [Windows Ribbon],IUIRibbon interface, scenicintent_IUIRibbon_SaveSettingsToStream, uiribbon/IUIRibbon::SaveSettingsToStream, windowsribbon.windowsribbon_iuiribbon_savesettingstostream
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIRibbon::SaveSettingsToStream
 - uiribbon/IUIRibbon::SaveSettingsToStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIRibbon.SaveSettingsToStream
---

# IUIRibbon::SaveSettingsToStream


## -description

Writes ribbon settings to a binary stream.

## -parameters

### -param pStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The stream is handed off to the host application for storage as appropriate.
			

The <b>SaveSettingsToStream</b> method is useful for persisting ribbon state, such as Quick Access Toolbar (QAT) items, across application instances.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon">IUIRibbon</a>



<a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream">IUIRibbon::LoadSettingsFromStream</a>



<a href="/windows/desktop/windowsribbon/ribbon-statepersistence">Persisting Ribbon State</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>