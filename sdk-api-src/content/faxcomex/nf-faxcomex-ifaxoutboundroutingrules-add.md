---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Add
title: IFaxOutboundRoutingRules::Add
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::Add method adds an outbound routing rule (IFaxOutboundRoutingRule interface) to the collection defined by the IFaxOutboundRoutingRules interface.
old-location: fax\_mfax_faxoutboundroutingrules_add_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_50f8_cpp.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxOutboundRoutingRules interface, IFaxOutboundRoutingRules interface [Fax Service],Add method, IFaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules::Add, _mfax_faxoutboundroutingrules.add_cpp, fax._mfax_faxoutboundroutingrules_add_cpp, faxcomex/IFaxOutboundRoutingRules::Add
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxOutboundRoutingRules.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingRules::Add


## -description


The <b>IFaxOutboundRoutingRules::Add</b> method adds an outbound routing rule (<a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface) to the collection defined by the <a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a> interface.


## -parameters




### -param lCountryCode

Type: <b>long</b>

A <b>long</b> value that specifies the country/region code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will add a rule that applies to any country/region code.


### -param lAreaCode

Type: <b>long</b>

Specifies a <b>long</b> value that indicates the area code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will add a rule that applies to any area code within the specified country/region code.


### -param bUseDevice

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value that indicates whether the outbound routing rule points to a single fax device rather than to a group of devices.


### -param bstrGroupName

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the outbound routing group to which the new routing rule belongs. If <i>bUseDevice</i> is set to <b>TRUE</b>, this should be an empty string.


### -param lDeviceId

Type: <b>long</b>

Specifies the device to associate with the outbound routing rule. If <i>bUseDevice</i> is set to <b>FALSE</b>, this parameter is ignored.


### -param pFaxOutboundRoutingRule [out, retval]

Type: <b><a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a>**</b>

An address of a pointer that receives a <a href="https://msdn.microsoft.com/29b577f6-6aeb-43fd-8a0f-657ef1c16999">IFaxOutboundRoutingRule</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can also return remote procedure call (RPC) return values. For more information, see <a href="_rpc_rpc_return_values">RPC Return Values</a>.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/35bb803d-fce4-46a3-825a-ec3a5138ed67">Visual Basic Example</a>
 

 

