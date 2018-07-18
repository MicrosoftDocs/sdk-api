---
UID: NF:azroles.IAzBizRuleInterfaces.AddInterfaces
title: IAzBizRuleInterfaces::AddInterfaces
author: windows-sdk-content
description: Adds the specified interfaces to the list of IDispatch interfaces that can be called by business rule (BizRule) scripts.
old-location: security\iazbizruleinterfaces_addinterfaces_method.htm
old-project: secauthz
ms.assetid: 91822c84-4daa-4d3c-bbe2-9ceb7fc642b2
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AddInterfaces, AddInterfaces method [Security], AddInterfaces method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],AddInterfaces method, IAzBizRuleInterfaces.AddInterfaces, IAzBizRuleInterfaces::AddInterfaces, azroles/IAzBizRuleInterfaces::AddInterfaces, security.iazbizruleinterfaces_addinterfaces_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzBizRuleInterfaces.AddInterfaces
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzBizRuleInterfaces::AddInterfaces


## -description


The <b>AddInterfaces</b> method adds the specified interfaces to the list of <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts. To add the specified interfaces, AzMan calls the <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface once for each specified interface.


## -parameters




### -param varInterfaceNames [in]

A <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that specifies the names that scripts use to call the interfaces specified by the <i>varInterfaces</i> array.


### -param varInterfaceFlags [in]

A <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that specifies flags sent to the <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface. The <b>AddNamedItem</b> always behaves as if the <b>SCRIPTITEM_ISVISIBLE</b> flag is set, and the <b>SCRIPTITEM_ISPERSISTENT</b> flag is not set.


### -param varInterfaces [in]

A <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> that specifies the IDs of the interfaces to be added.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The names of the interfaces specified by the <i>varInterfaceNames</i> array are in the same order as the corresponding interface IDs specified by the <i>varInterfaces</i> array.



