---
UID: NF:cluadmex.IGetClusterNetworkInfo.GetNetworkHandle
title: IGetClusterNetworkInfo::GetNetworkHandle
author: windows-sdk-content
description: Retrieves a handle to a network.
old-location: mscs\igetclusternetworkinfo_getnetworkhandle.htm
tech.root: mscs
ms.assetid: 596ebdb3-c4c1-4186-ac6b-e6a7d4a61688
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetNetworkHandle, GetNetworkHandle method [Failover Cluster], GetNetworkHandle method [Failover Cluster],IGetClusterNetworkInfo interface, IGetClusterNetworkInfo interface [Failover Cluster],GetNetworkHandle method, IGetClusterNetworkInfo.GetNetworkHandle, IGetClusterNetworkInfo::GetNetworkHandle, _wolf_igetclusternetworkinfo_getnetworkhandle, cluadmex/IGetClusterNetworkInfo::GetNetworkHandle, mscs.igetclusternetworkinfo_getnetworkhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
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
 - cluadmex.h
api_name:
 - IGetClusterNetworkInfo.GetNetworkHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterNetworkInfo::GetNetworkHandle


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Retrieves a handle to a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target network. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>.


## -returns



If <b>GetNetworkHandle</b> is 
       successful, it returns a handle for the network represented by <i>lObjIndex</i>.

If <b>GetNetworkHandle</b> is not 
       successful, it returns <b>NULL</b>. For more information about the error, call the function 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not close the handle obtained through this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>
 

 

