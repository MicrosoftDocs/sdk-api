---
UID: NF:wmpservices.IWMPServices.GetStreamState
title: IWMPServices::GetStreamState
author: windows-driver-content
description: The IWMPServices::GetStreamState method retrieves information about the current play state of the stream.
old-location: wmp\iwmpservices_getstreamstate.htm
old-project: WMP
ms.assetid: 1a73ea54-45ce-47ff-b551-10aab2798420
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetStreamState, GetStreamState method [Windows Media Player], GetStreamState method [Windows Media Player],IWMPServices interface, IWMPServices interface [Windows Media Player],GetStreamState method, IWMPServices.GetStreamState, IWMPServices::GetStreamState, IWMPServicesGetStreamStateDSP, wmp.iwmpservices_getstreamstate, wmpservices/IWMPServices::GetStreamState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPServices.GetStreamState
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPServices::GetStreamState


## -description



The <b>IWMPServices::GetStreamState</b> method retrieves information about the current play state of the stream.




## -parameters




### -param pState [in]

A pointer to a <b>WMPServices_StreamState</b> enumeration value.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



The stream is stopped, paused, or playing.




## -see-also




<a href="https://msdn.microsoft.com/26d68b4b-4eeb-42e2-a1d1-0d0e73725059">IWMPServices Interface</a>



<a href="https://msdn.microsoft.com/82c4699a-197c-4429-afa8-b1fc47a1f47a">WMPServices_StreamState</a>
 

 

