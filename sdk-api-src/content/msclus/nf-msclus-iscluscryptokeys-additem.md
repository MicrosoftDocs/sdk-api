---
UID: NF:msclus.ISClusCryptoKeys.AddItem
title: ISClusCryptoKeys::AddItem
author: windows-sdk-content
description: Adds a crypto key to a ClusCryptoKeys collection.
old-location: mscs\cluscryptokeys_additem.htm
old-project: mscs
ms.assetid: 4f830e93-fa0a-4dbe-9544-9065cb2b4e8d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddItem, AddItem method [Failover Cluster], AddItem method [Failover Cluster],ClusCryptoKeys class, ClusCryptoKeys class [Failover Cluster],AddItem method, ClusCryptoKeys.AddItem, ISClusCryptoKeys.AddItem, ISClusCryptoKeys::AddItem, _wolf_cluscryptokeys.additem, mscs.cluscryptokeys_additem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusCryptoKeys.AddItem
 - ISClusCryptoKeys.AddItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusCryptoKeys::AddItem


## -description


<p class="CCE_Message">[The <b>AddItem</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Adds a crypto key 
    to a <a href="https://msdn.microsoft.com/0078ba7a-24d7-4de6-af05-f1a03d9deb0a">ClusCryptoKeys</a> 
    collection.


## -parameters




### -param bstrCryptoKey






#### - strName

String identifying the cryptographic service provider (CSP) key container to be checkpointed. The CSP key 
        container must first be created with the <a href="https://msdn.microsoft.com/9ccce1b6-4a53-41fd-92f0-c1ed48320781">Cryptography API</a>, 
        and the keys in the container must be exportable. The string must specify the CSP provider type, provider 
        name, and key container name using the following syntax.

<i>Type</i>\<i>Name</i>\<i>Key</i>

Note that the values must be separated by a '\'. The provider type should specify the decimal value of the 
        type, not the constant that represents the value. For example, instead of "PROV_RSA_FULL" use 
        "1". The provider name is optional, and if it is omitted, the default CSP provider name 
        associated with the specified provider type will be used.


## -returns



A string that receives the added key.




## -remarks



For more information on the following points, see the 
    <a href="https://msdn.microsoft.com/9ccce1b6-4a53-41fd-92f0-c1ed48320781">Cryptography Reference</a>.

<ul>
<li>A key container is given a name when it is created using 
      <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> with 
      <i>dwFlags</i> set to <b>CRYPT_NEWKEYSET</b>.</li>
<li>Once a key container has been created, the key pairs for that key container must be created using 
      <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> with the 
      <i>dwFlags</i> parameter set to <b>CRYPT_EXPORTABLE</b>. Note that some 
      CSPs do not allow key exports from their key containers. If a key is not exportable then the 
      <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> call will fail with an 
      <b>NTE_BAD_KEY</b> error.</li>
</ul>
For more information on checkpoints, see 
    <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">Checkpointing</a>.




## -see-also




<a href="https://msdn.microsoft.com/0078ba7a-24d7-4de6-af05-f1a03d9deb0a">ClusCryptoKeys</a>



<a href="https://msdn.microsoft.com/8c285882-915c-45de-9840-cfc5becd55ee">ClusProperty</a>
 

 

