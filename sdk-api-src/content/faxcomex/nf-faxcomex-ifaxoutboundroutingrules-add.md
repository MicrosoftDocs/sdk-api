---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Add
title: IFaxOutboundRoutingRules::Add
author: windows-sdk-content
description: The Add method adds an outbound routing rule (FaxOutboundRoutingRule object) to the FaxOutboundRoutingRules collection.
old-location: fax\_mfax_faxoutboundroutingrules_add.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_50f8.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],FaxOutboundRoutingRules object, FaxOutboundRoutingRules object [Fax Service],Add method, FaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules::Add, _mfax_faxoutboundroutingrules.add, fax._mfax_faxoutboundroutingrules_add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxOutboundRoutingRules.Add
 - IFaxOutboundRoutingRules.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxOutboundRoutingRules::Add


## -description


The <b>Add</b> method adds an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) to the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection.


## -parameters




### -param lCountryCode

Type: <b>Long</b>

A <b>Long</b> value that specifies the country/region code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will add a rule that applies to any country/region code.


### -param lAreaCode

Type: <b>Long</b>

Specifies a <b>Long</b> value that indicates the area code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will add a rule that applies to any area code within the specified country/region code.


### -param bUseDevice

Type: <b>Boolean</b>

Specifies a Boolean value that indicates whether the outbound routing rule points to a single fax device rather than to a group of devices.


### -param bstrGroupName

Type: <b>String</b>

Specifies a null-terminated string that contains the name of the outbound routing group to which the new routing rule belongs. If <i>bUseDevice</i> is set to <b>True</b>, this should be an empty string.


### -param lDeviceId

Type: <b>Long</b>

Specifies the device to associate with the outbound routing rule. If <i>bUseDevice</i> is set to <b>False</b>, this parameter is ignored.


### -param pFaxOutboundRoutingRule






## -returns



Type: <b><a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a>**</b>

A <a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object.




## -remarks



This method can also return remote procedure call (RPC) return values. For more information, see <a href="_rpc_rpc_return_values">RPC Return Values</a>.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/35bb803d-fce4-46a3-825a-ec3a5138ed67">Visual Basic Example</a>
 

 

