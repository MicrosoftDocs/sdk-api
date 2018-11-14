---
UID: NF:bits3_0.IBitsPeerCacheAdministration.EnumPeers
title: IBitsPeerCacheAdministration::EnumPeers
author: windows-sdk-content
description: Gets an IEnumBitsPeers interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.
old-location: bits\ibitspeercacheadministration_enumpeers.htm
tech.root: Bits
ms.assetid: 8786d7d8-9ffb-4492-9834-90b97f97e4cf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnumPeers, EnumPeers method [BITS], EnumPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],EnumPeers method, IBitsPeerCacheAdministration.EnumPeers, IBitsPeerCacheAdministration::EnumPeers, bits.ibitspeercacheadministration_enumpeers, bits3_0/IBitsPeerCacheAdministration::EnumPeers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.EnumPeers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bits3_0.h
: 
- IBitsPeerCacheAdministration.EnumPeers
: 
---

# IBitsPeerCacheAdministration::EnumPeers


## -description


Gets an <a href="https://msdn.microsoft.com/en-us/library/Aa964308(v=VS.85).aspx">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.


## -parameters




### -param ppEnum [out]

An <a href="https://msdn.microsoft.com/en-us/library/Aa964308(v=VS.85).aspx">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. Release <i>ppEnum</i> when done.


## -returns



This method returns S_OK on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964273(v=VS.85).aspx">IBitsPeerCacheAdministration::ClearPeers</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964277(v=VS.85).aspx">IBitsPeerCacheAdministration::DiscoverPeers</a>
 

 

