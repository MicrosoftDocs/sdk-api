---
UID: NF:uiribbon.IUIRibbon.LoadSettingsFromStream
title: IUIRibbon::LoadSettingsFromStream (uiribbon.h)
author: windows-sdk-content
description: Reads ribbon settings from a binary stream.
old-location: windowsribbon\windowsribbon_iuiribbon_loadsettingsfromstream.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\loadsettingsfromstream.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIRibbon interface [Windows Ribbon],LoadSettingsFromStream method, IUIRibbon.LoadSettingsFromStream, IUIRibbon::LoadSettingsFromStream, LoadSettingsFromStream, LoadSettingsFromStream method [Windows Ribbon], LoadSettingsFromStream method [Windows Ribbon],IUIRibbon interface, scenicintent_IUIRibbon_LoadSettingsFromStream, uiribbon/IUIRibbon::LoadSettingsFromStream, windowsribbon.windowsribbon_iuiribbon_loadsettingsfromstream
ms.topic: method
f1_keywords: 
 - "uiribbon/IUIRibbon.LoadSettingsFromStream"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIRibbon.LoadSettingsFromStream
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
---

# IUIRibbon::LoadSettingsFromStream


## -description


Reads ribbon settings from a binary stream.
		


## -parameters




### -param pStream [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object. 
				


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_FAIL if the format or content of the serialized stream 
						is empty or cannot be verified by the Ribbon framework.
					




## -remarks



The stream is supplied by the host application.
			
				If the Windows Ribbon framework is unable to load a valid stream, the default ribbon layout is rendered instead.
			

The <b>LoadSettingsFromStream </b> method is useful for persisting ribbon state, such as Quick Access Toolbar (QAT) items, across application instances. 
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon">IUIRibbon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream">IUIRibbon::SaveSettingsToStream</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/ribbon-statepersistence">Persisting Ribbon State</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
 

 

