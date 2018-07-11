---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Add
title: IFaxOutboundRoutingRules::Add
author: windows-sdk-content
description: The Add method adds an outbound routing rule (FaxOutboundRoutingRule object) to the FaxOutboundRoutingRules collection.
old-location: fax\_mfax_faxoutboundroutingrules_add.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_50f8.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],FaxOutboundRoutingRules object, FaxOutboundRoutingRules object [Fax Service],Add method, FaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules::Add, _mfax_faxoutboundroutingrules.add, fax._mfax_faxoutboundroutingrules_add
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


The <b>Add</b> method adds an outbound routing rule (<a href="https://msdn.microsoft.com/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a> object) to the <a href="https://msdn.microsoft.com/library/ms689525(v=VS.85).aspx">FaxOutboundRoutingRules</a> collection.


## -parameters




### -param lCountryCode

Type: <b>Long</b>

A <b>Long</b> value that specifies the country/region code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/library/ms687973(v=VS.85).aspx">frrcANY_CODE</a> will add a rule that applies to any country/region code.


### -param lAreaCode

Type: <b>Long</b>

Specifies a <b>Long</b> value that indicates the area code to associate with the outbound routing rule. Specifying <a href="https://msdn.microsoft.com/library/ms687973(v=VS.85).aspx">frrcANY_CODE</a> will add a rule that applies to any area code within the specified country/region code.


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



Type: <b><a href="https://msdn.microsoft.com/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a>**</b>

A <a href="https://msdn.microsoft.com/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a> object.




## -remarks



This method can also return remote procedure call (RPC) return values. For more information, see <a href="https://msdn.microsoft.com/library/Aa378645(v=VS.85).aspx">RPC Return Values</a>.

To read or to write to this property, a user must have the <a href="https://msdn.microsoft.com/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/library/ms689525(v=VS.85).aspx">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/library/ms689527(v=VS.85).aspx">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/library/ms693486(v=VS.85).aspx">Visual Basic Example</a>
 

 

