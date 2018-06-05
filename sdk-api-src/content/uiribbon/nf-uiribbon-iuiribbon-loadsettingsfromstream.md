---
UID: NF:uiribbon.IUIRibbon.LoadSettingsFromStream
title: IUIRibbon::LoadSettingsFromStream
author: windows-sdk-content
description: Reads ribbon settings from a binary stream.
old-location: windowsribbon\windowsribbon_iuiribbon_loadsettingsfromstream.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiribbon\loadsettingsfromstream.htm
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IUIRibbon interface [Windows Ribbon],LoadSettingsFromStream method, IUIRibbon.LoadSettingsFromStream, IUIRibbon::LoadSettingsFromStream, LoadSettingsFromStream, LoadSettingsFromStream method [Windows Ribbon], LoadSettingsFromStream method [Windows Ribbon],IUIRibbon interface, scenicintent_IUIRibbon_LoadSettingsFromStream, uiribbon/IUIRibbon::LoadSettingsFromStream, windowsribbon.windowsribbon_iuiribbon_loadsettingsfromstream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mshtml.dll
api_name:
-	IUIRibbon.LoadSettingsFromStream
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/6a43f17b-dbf6-4c5b-818f-c0dde896de99">IUIRibbon</a>



<a href="https://msdn.microsoft.com/b5cd7cfd-95b7-49a1-8931-8befef7d4298">IUIRibbon::SaveSettingsToStream</a>



<a href="https://msdn.microsoft.com/f59e36be-8e3d-454a-b93c-9fc5fc5ecb47">Persisting Ribbon State</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

