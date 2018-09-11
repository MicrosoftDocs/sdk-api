---
UID: NF:uiribbon.IUIRibbon.LoadSettingsFromStream
title: IUIRibbon::LoadSettingsFromStream
author: windows-sdk-content
description: Reads ribbon settings from a binary stream.
old-location: windowsribbon\windowsribbon_iuiribbon_loadsettingsfromstream.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\loadsettingsfromstream.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIRibbon interface [Windows Ribbon],LoadSettingsFromStream method, IUIRibbon.LoadSettingsFromStream, IUIRibbon::LoadSettingsFromStream, LoadSettingsFromStream, LoadSettingsFromStream method [Windows Ribbon], LoadSettingsFromStream method [Windows Ribbon],IUIRibbon interface, scenicintent_IUIRibbon_LoadSettingsFromStream, uiribbon/IUIRibbon::LoadSettingsFromStream, windowsribbon.windowsribbon_iuiribbon_loadsettingsfromstream
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIRibbon.LoadSettingsFromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
---

# IUIRibbon::LoadSettingsFromStream


## -description


Reads ribbon settings from a binary stream.
		


## -parameters




### -param pStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object. 
				


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_FAIL if the format or content of the serialized stream 
						is empty or cannot be verified by the Ribbon framework.
					




## -remarks



The stream is supplied by the host application.
			
				If the Windows Ribbon framework is unable to load a valid stream, the default ribbon layout is rendered instead.
			

The <b>LoadSettingsFromStream </b> method is useful for persisting ribbon state, such as Quick Access Toolbar (QAT) items, across application instances. 
			




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371360(v=VS.85).aspx">IUIRibbon</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371362(v=VS.85).aspx">IUIRibbon::SaveSettingsToStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee264330(v=VS.85).aspx">Persisting Ribbon State</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 

