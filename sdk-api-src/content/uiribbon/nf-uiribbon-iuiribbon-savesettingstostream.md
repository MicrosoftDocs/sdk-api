---
UID: NF:uiribbon.IUIRibbon.SaveSettingsToStream
title: IUIRibbon::SaveSettingsToStream
author: windows-sdk-content
description: Writes ribbon settings to a binary stream.
old-location: windowsribbon\windowsribbon_iuiribbon_savesettingstostream.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\savesettingstostream.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIRibbon interface [Windows Ribbon],SaveSettingsToStream method, IUIRibbon.SaveSettingsToStream, IUIRibbon::SaveSettingsToStream, SaveSettingsToStream, SaveSettingsToStream method [Windows Ribbon], SaveSettingsToStream method [Windows Ribbon],IUIRibbon interface, scenicintent_IUIRibbon_SaveSettingsToStream, uiribbon/IUIRibbon::SaveSettingsToStream, windowsribbon.windowsribbon_iuiribbon_savesettingstostream
ms.topic: method
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
 - IUIRibbon.SaveSettingsToStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
---

# IUIRibbon::SaveSettingsToStream


## -description


Writes ribbon settings to a binary stream.
		


## -parameters




### -param pStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The stream is handed off to the host application for storage as appropriate.
			

The <b>SaveSettingsToStream</b> method is useful for persisting ribbon state, such as Quick Access Toolbar (QAT) items, across application instances.
			




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371360(v=VS.85).aspx">IUIRibbon</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371361(v=VS.85).aspx">IUIRibbon::LoadSettingsFromStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee264330(v=VS.85).aspx">Persisting Ribbon State</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

