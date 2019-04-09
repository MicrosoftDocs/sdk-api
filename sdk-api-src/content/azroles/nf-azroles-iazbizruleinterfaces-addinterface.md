---
UID: NF:azroles.IAzBizRuleInterfaces.AddInterface
title: IAzBizRuleInterfaces::AddInterface (azroles.h)
author: windows-sdk-content
description: Adds the specified interface to the list of IDispatch interfaces that can be called by business rule (BizRule) scripts.
old-location: security\iazbizruleinterfaces_addinterface.htm
tech.root: SecAuthZ
ms.assetid: 063492b9-9970-4605-84f5-d8b80afc719b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddInterface, AddInterface method [Security], AddInterface method [Security],IAzBizRuleInterfaces interface, IAzBizRuleInterfaces interface [Security],AddInterface method, IAzBizRuleInterfaces.AddInterface, IAzBizRuleInterfaces::AddInterface, azroles/IAzBizRuleInterfaces::AddInterface, security.iazbizruleinterfaces_addinterface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzBizRuleInterfaces.AddInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzBizRuleInterfaces::AddInterface


## -description


The <b>AddInterface</b> method adds the specified interface to the list of <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts. To add the specified interface, AzMan calls the  <a href="https://msdn.microsoft.com/library/s8eyc3sh(v=VS.85).aspx">AddNamedItem</a> method of the <a href="https://msdn.microsoft.com/library/ky29ffxd(v=VS.85).aspx">IActiveScript</a> interface.


## -parameters




### -param bstrInterfaceName [in]

A string that contains the name used by scripts to call the interface specified by the <i>varInterface</i> parameter.


### -param lInterfaceFlag [in]

Flags sent to the <a href="https://msdn.microsoft.com/library/s8eyc3sh(v=VS.85).aspx">AddNamedItem</a> method of the <a href="https://msdn.microsoft.com/library/ky29ffxd(v=VS.85).aspx">IActiveScript</a> interface. The <b>AddNamedItem</b> always behaves as if the <b>SCRIPTITEM_ISVISIBLE</b> flag is set, and the <b>SCRIPTITEM_ISPERSISTENT</b> flag is not set.


### -param varInterface [in]

The ID of the interface to be added.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/96cc0e45-ddd5-4ab0-9243-5f2046e48f78">IAzBizRuleInterfaces</a>
 

 

