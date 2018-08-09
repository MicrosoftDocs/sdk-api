---
UID: NF:msclus.ISClusRegistryKeys.AddItem
title: ISClusRegistryKeys::AddItem
author: windows-sdk-content
description: Adds a registry key to a ClusRegistryKeys collection.
old-location: mscs\clusregistrykeys_additem.htm
old-project: mscs
ms.assetid: 8b28b848-ab26-4422-9e0e-a47613d7aa63
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddItem, AddItem method [Failover Cluster], AddItem method [Failover Cluster],ClusRegistryKeys class, ClusRegistryKeys class [Failover Cluster],AddItem method, ClusRegistryKeys.AddItem, ISClusRegistryKeys.AddItem, ISClusRegistryKeys::AddItem, _wolf_clusregistrykeys.additem, mscs.clusregistrykeys_additem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusRegistryKeys.AddItem
 - ISClusRegistryKeys.AddItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusRegistryKeys::AddItem


## -description


<p class="CCE_Message">[The <b>AddItem</b> method 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Adds a registry 
    key to a <a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a> 
    collection.


## -parameters




### -param bstrRegistryKey






#### - strName

String identifying the new key.


## -returns



A string that receives the added key.




## -remarks



For more information on checkpoints, see 
    <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a>.


#### Examples

Use the <b>AddItem</b> method to add a registry 
     key to a resource's list of checkpointed registry keys.

<div class="code"></div>
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Public Function AddKey(ByRef objRes as ClusResource, _
                       ByVal strKey as String)

  Dim colRegKeys as ClusRegistryKeys
  Set colRegKeys = objRes.RegistryKeys
  colRegKeys.AddItem( strKey )
  Set colRegKeys = Nothing

End Function
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>



<a href="https://msdn.microsoft.com/888f70d9-6562-4add-895d-604f22d75307">ClusRegistryKeys</a>
 

 

