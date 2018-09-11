---
UID: NF:faxcomex.IFaxDevice.UseRoutingMethod
title: IFaxDevice::UseRoutingMethod
author: windows-sdk-content
description: The IFaxDevice::UseRoutingMethod method adds an inbound fax routing method to or removes a fax routing method (FaxInboundRoutingMethod) from the list of routing methods associated with the fax device.
old-location: fax\_mfax_faxdevice_cpp_mfax_faxdevice_useroutingmethod_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2m90.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxDevice interface [Fax Service],UseRoutingMethod method, IFaxDevice.UseRoutingMethod, IFaxDevice::UseRoutingMethod, UseRoutingMethod, UseRoutingMethod method [Fax Service], UseRoutingMethod method [Fax Service],IFaxDevice interface, _mfax_faxdevice.useroutingmethod, fax._mfax_faxdevice_cpp_mfax_faxdevice_useroutingmethod_cpp, fax._mfax_faxdevice_useroutingmethod, faxcomex/IFaxDevice::UseRoutingMethod
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDevice.UseRoutingMethod
 - IFaxDevice.UseRoutingMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice::UseRoutingMethod


## -description


The <b>IFaxDevice::UseRoutingMethod</b> method adds an inbound fax routing method to or removes a fax routing method (<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>) from the list of routing methods associated with the fax device.


## -parameters




### -param bstrMethodGUID [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that uniquely identifies the fax routing method to add or remove.


### -param bUse [in]

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value. If this parameter is equal to <b>TRUE</b>, the method adds the fax routing method to the list of inbound methods associated with the fax device. If you set this parameter to <b>FALSE</b>, the method removes the routing method from the list.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a>



<a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

