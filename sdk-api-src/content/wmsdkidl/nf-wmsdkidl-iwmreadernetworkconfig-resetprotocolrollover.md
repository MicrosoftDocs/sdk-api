---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.ResetProtocolRollover
title: IWMReaderNetworkConfig::ResetProtocolRollover
author: windows-sdk-content
description: The ResetProtocolRollover method forces the reader object to use the normal protocol rollover algorithm.
old-location: wmformat\iwmreadernetworkconfig_resetprotocolrollover.htm
tech.root: wmformat
ms.assetid: 10a11131-48bd-49bd-a767-1c6148f84b95
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],ResetProtocolRollover method, IWMReaderNetworkConfig.ResetProtocolRollover, IWMReaderNetworkConfig::ResetProtocolRollover, IWMReaderNetworkConfigResetProtocolRollover, ResetProtocolRollover, ResetProtocolRollover method [windows Media Format], ResetProtocolRollover method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_resetprotocolrollover, wmsdkidl/IWMReaderNetworkConfig::ResetProtocolRollover
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderNetworkConfig.ResetProtocolRollover
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig::ResetProtocolRollover


## -description



The <b>ResetProtocolRollover</b> method forces the reader object to use the normal protocol rollover algorithm.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Protocol rollover is a process whereby the reader object discovers the best streaming protocol available from a server. For more information, see <a href="https://msdn.microsoft.com/61db5e2b-4858-446e-9a27-e0305b46683d">Protocol Rollover</a>.

When the reader object uses protocol rollover, it records which protocol was used and tries that protocol first on subsequent connection attempts. After a certain period of time, the reader object goes back to the default protocol rollover behavior.

However, if the application disables a particular protocol (for example, by calling <b>SetEnableUDP</b> or <b>SetEnableTCP</b>), the reader object may use a protocol that is less efficient than necessary. You can force the reader object to use the default protocol rollover behavior by calling the <b>ResetProtocolRollover</b> method.

Player users sometimes experiment with network settings when they are having connectivity problems. By using this method to reset the protocol rollover settings, the application can improve the quality of streaming that users receive.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/03afdef3-2aa8-4826-8dce-6d501fa42bcd">IWMReaderNetworkConfig::SetEnableUDP</a>
 

 

