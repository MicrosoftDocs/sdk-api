---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IAzBizRuleInterfaces::AddInterface


## -description


The <b>AddInterface</b> method adds the specified interface to the list of <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interfaces that can be called by business rule (BizRule) scripts. To add the specified interface, AzMan calls the  <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface.


## -parameters




### -param bstrInterfaceName [in]

A string that contains the name used by scripts to call the interface specified by the <i>varInterface</i> parameter.


### -param lInterfaceFlag [in]

Flags sent to the <a href="a7c6317d-948f-4bb3-b169-1bbe5b7c7cc5">AddNamedItem</a> method of the <a href="d8acee11-7f0d-4999-b97a-66774af16f71">IActiveScript</a> interface. The <b>AddNamedItem</b> always behaves as if the <b>SCRIPTITEM_ISVISIBLE</b> flag is set, and the <b>SCRIPTITEM_ISPERSISTENT</b> flag is not set.


### -param varInterface [in]

The ID of the interface to be added.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/96cc0e45-ddd5-4ab0-9243-5f2046e48f78">IAzBizRuleInterfaces</a>
 

 

