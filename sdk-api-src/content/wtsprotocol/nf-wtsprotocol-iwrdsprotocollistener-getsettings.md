---
UID: NF:wtsprotocol.IWRdsProtocolListener.GetSettings
title: IWRdsProtocolListener::GetSettings method
author: windows-driver-content
description: Gets the listener setting information for client connection requests.
old-location: termserv\iwrdsprotocollistener_getsettings.htm
old-project: TermServ
ms.assetid: 644eaa8f-776d-49de-af23-de9faef80e74
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetSettings method [Remote Desktop Services], GetSettings method [Remote Desktop Services], IWRdsProtocolListener interface, GetSettings,IWRdsProtocolListener.GetSettings, IWRdsProtocolListener, IWRdsProtocolListener interface [Remote Desktop Services], GetSettings method, IWRdsProtocolListener::GetSettings, termserv.iwrdsprotocollistener_getsettings, wtsprotocol/IWRdsProtocolListener::GetSettings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWRdsProtocolListener.GetSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolListener::GetSettings method


## -description


Gets the listener setting information for client connection requests.


## -parameters




### -param WRdsListenerSettingLevel [in]

The listener setting level to use.


### -param pWRdsListenerSettings [out]

A pointer to a <a href="https://msdn.microsoft.com/75C9C9AF-9C27-402C-886D-269BF567825F">WRDS_LISTENER_SETTINGS</a> structure that contains the returned listener settings.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a>
 

 

