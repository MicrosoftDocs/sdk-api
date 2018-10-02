---
UID: NF:cluadmex.IGetClusterResourceInfo.GetResourceTypeName
title: IGetClusterResourceInfo::GetResourceTypeName
author: windows-sdk-content
description: Returns the type of a resource.
old-location: mscs\igetclusterresourceinfo_getresourcetypename.htm
tech.root: MsCS
ms.assetid: c7154163-0ab9-4766-99be-31457a0efc17
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetResourceTypeName, GetResourceTypeName method [Failover Cluster], GetResourceTypeName method [Failover Cluster],IGetClusterResourceInfo interface, IGetClusterResourceInfo interface [Failover Cluster],GetResourceTypeName method, IGetClusterResourceInfo.GetResourceTypeName, IGetClusterResourceInfo::GetResourceTypeName, _wolf_igetclusterresourceinfo_getresourcetypename, cluadmex/IGetClusterResourceInfo::GetResourceTypeName, mscs.igetclusterresourceinfo_getresourcetypename
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
 - IGetClusterResourceInfo.GetResourceTypeName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterResourceInfo::GetResourceTypeName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the type of a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target resource. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>.


### -param lpszResTypeName [out]

Pointer to the type of the resource associated with <i>lObjIndex</i>. The 
       <i>lpResTypeName</i> parameter can be <b>NULL</b>, indicating that the 
       caller is requesting only the length of the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a>. Although declared as a 
       <b>BSTR</b>, this parameter is implemented as an <b>LPWSTR</b>.


### -param pcchResTypeName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpResTypeName</i> parameter. The <i>pcchResTypeName</i> parameter 
       cannot be <b>NULL</b>. On output, pointer to the count of characters in the resource type 
       name stored in the content of <i>lpResTypeName</i>, including the 
       <b>NULL</b>-terminating character.


## -returns



If <b>GetResourceTypeName</b> 
       is not successful, it can return other <b>HRESULT</b> values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>
 

 

