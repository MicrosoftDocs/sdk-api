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

# IMetaDataDispenserEx::GetOption


## -description


Gets the value of the specified option for the current metadata scope. The option controls how calls to the current metadata scope are handled.


## -parameters




### -param optionId [in]

A pointer to a GUID that specifies the option to be retrieved. See the Remarks section for a list of supported GUIDs.


### -param pValue [out]

The value of the returned option. The type of this value will be a variant of the specified option's type.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following list shows the GUIDs that are supported for this method. For descriptions, see the <a href="https://msdn.microsoft.com/bb84abf1-0bba-4f9d-98fb-3ed67819a9dc">SetOption</a> method. If <i>optionId</i> is not in this list, this method returns HRESULT <b>E_INVALIDARG</b>, indicating an incorrect parameter.

<ul>
<li>
MetaDataCheckDuplicatesFor

</li>
<li>
MetaDataRefToDefCheck

</li>
<li>
MetaDataNotificationForTokenMovement

</li>
<li>
MetaDataSetENC

</li>
<li>
MetaDataErrorIfEmitOutOfOrder

</li>
<li>
MetaDataGenerateTCEAdapters

</li>
<li>
MetaDataLinkerOptions

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b61c8d05-6d73-4f84-95b2-2a892f3de77c">IMetaDataDispenserEx</a>
 

 

