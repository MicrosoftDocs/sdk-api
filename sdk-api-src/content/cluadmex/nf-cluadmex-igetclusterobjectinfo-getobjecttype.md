---
UID: NF:cluadmex.IGetClusterObjectInfo.GetObjectType
title: IGetClusterObjectInfo::GetObjectType
author: windows-sdk-content
description: Returns the type of a cluster object.
old-location: mscs\igetclusterobjectinfo_getobjecttype.htm
tech.root: mscs
ms.assetid: f01a1ada-bb4d-4042-ac56-3658262d1110
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetObjectType, GetObjectType method [Failover Cluster], GetObjectType method [Failover Cluster],IGetClusterObjectInfo interface, IGetClusterObjectInfo interface [Failover Cluster],GetObjectType method, IGetClusterObjectInfo.GetObjectType, IGetClusterObjectInfo::GetObjectType, _wolf_igetclusterobjectinfo_getobjecttype, cluadmex/IGetClusterObjectInfo::GetObjectType, mscs.igetclusterobjectinfo_getobjecttype
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
 - IGetClusterObjectInfo.GetObjectType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterObjectInfo::GetObjectType


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Returns the type of a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster object</a>.


## -parameters




### -param lObjIndex [in]

A number representing the zero-based index of the target object. This parameter is restricted to the number 
       that can be retrieved by calling 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>.


## -returns




If <a href="https://msdn.microsoft.com/en-us/library/Aa370229(v=VS.85).aspx">GetObjectType</a> is 
        successful, it returns one of the following values enumerated by the 
        <b>CLUADMEX_OBJECT_TYPE</b> enumeration representing the object types:



If <b>GetObjectType</b> is not 
       successful, it returns –1. For more information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>CLUADMEX_OT_NONE</b> is returned when 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> does not recognize 
     the object type.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">IGetClusterDataInfo::GetObjectCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>
 

 

