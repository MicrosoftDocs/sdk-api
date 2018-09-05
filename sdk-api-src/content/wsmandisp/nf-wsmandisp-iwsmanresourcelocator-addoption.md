---
UID: NF:wsmandisp.IWSManResourceLocator.AddOption
title: IWSManResourceLocator::AddOption
author: windows-sdk-content
description: Adds data required to process the request. For example, some WMI providers may require an IWbemContext or SWbemNamedValueSet object with provider-specific information.
old-location: winrm\iwsmanresourcelocator_addoption.htm
old-project: WinRM
ms.assetid: a6709cb7-35a1-41b6-981e-13d3f1bf9816
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddOption, AddOption method [Windows Remote Management], AddOption method [Windows Remote Management],IWSManResourceLocator interface, IWSManResourceLocator interface [Windows Remote Management],AddOption method, IWSManResourceLocator.AddOption, IWSManResourceLocator::AddOption, winrm.iwsmanresourcelocator_addoption, wsmandisp/IWSManResourceLocator::AddOption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManResourceLocator.AddOption
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManResourceLocator::AddOption


## -description


Adds data required to process the request. For example, some WMI providers may require an <a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> or <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object with provider-specific information. You can provide a <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">ResourceLocator</a> object instead of specifying a resource URI in <a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a> object operations such as <a href="https://msdn.microsoft.com/f6393cfb-0787-4d30-8d02-be0996885f22">Get</a>, <a href="https://msdn.microsoft.com/1224dab8-82d1-4416-8c21-e84fdda15deb">Put</a>, or <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">Enumerate</a>.

    
    
  


## -parameters




### -param OptionName [in]

The name of the optional data object.


### -param OptionValue [in]

A value supplied for the optional data object.


### -param mustComply [in]

A flag that indicates the option must be processed. The default is <b>False</b> (0).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>



<a href="https://msdn.microsoft.com/c85949fc-41e7-47eb-8aab-9b456490bc81">ResourceLocator.AddOption</a>
 

 

