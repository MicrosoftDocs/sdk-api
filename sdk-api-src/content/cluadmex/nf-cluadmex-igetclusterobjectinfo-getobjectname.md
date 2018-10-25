---
UID: NF:cluadmex.IGetClusterObjectInfo.GetObjectName
title: IGetClusterObjectInfo::GetObjectName
author: windows-sdk-content
description: Returns the name of a cluster object.
old-location: mscs\igetclusterobjectinfo_getobjectname.htm
tech.root: mscs
ms.assetid: e45f3652-74da-4d93-826d-320ddae10f49
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: GetObjectName, GetObjectName method [Failover Cluster], GetObjectName method [Failover Cluster],IGetClusterObjectInfo interface, IGetClusterObjectInfo interface [Failover Cluster],GetObjectName method, IGetClusterObjectInfo.GetObjectName, IGetClusterObjectInfo::GetObjectName, _wolf_igetclusterobjectinfo_getobjectname, cluadmex/IGetClusterObjectInfo::GetObjectName, mscs.igetclusterobjectinfo_getobjectname
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
 - IGetClusterObjectInfo.GetObjectName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterObjectInfo::GetObjectName


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the name of a <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster object</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target object. <i>lObjIndex</i> is 
       restricted to the number that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>.


### -param lpszName [out]

Pointer to a null-terminated Unicode string containing the name of the object associated with 
       <i>lObjIndex</i>. The <i>lpszName</i> parameter can be 
       <b>NULL</b>, indicating that the caller is requesting only the name length. Although 
       declared as a <b>BSTR</b>, this parameter is implemented as an 
       <b>LPWSTR</b>.


### -param pcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszName</i> parameter. The <i>pcchName</i> parameter cannot be 
       <b>NULL</b>. On output, pointer to the count of characters in the name stored in the content 
       of <i>lpszName</i>, including the <b>NULL</b>-terminating character.


## -returns



If <b>GetObjectName</b> is not 
       successful, it can return other <b>HRESULT</b> values.




## -remarks



If the <i>lpszName</i> parameter is specified as <b>NULL</b>, the 
     <b>GetObjectName</b> method returns 
     <b>NOERROR</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>
 

 

