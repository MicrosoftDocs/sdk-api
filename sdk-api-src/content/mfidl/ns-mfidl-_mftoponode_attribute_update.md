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

# _MFTOPONODE_ATTRIBUTE_UPDATE structure


## -description


Specifies a new attribute value for a topology node.


## -struct-fields




### -field NodeId


            The identifier of the topology node to update. To get the identifier of a topology node, call <a href="https://msdn.microsoft.com/9c0e5be9-6481-4132-ad5b-9db13fb07391">IMFTopologyNode::GetTopoNodeID</a>.
          


### -field guidAttributeKey


            GUID that specifies the attribute to update.
          


### -field attrType


            Attribute type, specified as a member of the <a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a> enumeration.
          


### -field u32


              Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT32</b>.
            


### -field u64


              Attribute value (unsigned 32-bit integer). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_UINT64</b>. See Remarks.
            


### -field d


              Attribute value (floating point). This member is used when <b>attrType</b> equals <b>MF_ATTRIBUTE_DOUBLE</b>.
            


## -remarks




        Due to an error in the structure declaration, the <b>u64</b> member is declared as a 32-bit integer, not a 64-bit integer. Therefore, any 64-bit value passed to the <a href="https://msdn.microsoft.com/a769b0bd-a43f-478b-a6e4-bbef05942616">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a> method is truncated to 32 bits.
      




## -see-also




<a href="https://msdn.microsoft.com/a769b0bd-a43f-478b-a6e4-bbef05942616">IMFTopologyNodeAttributeEditor::UpdateNodeAttributes</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>
 

 

