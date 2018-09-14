---
UID: NF:iads.IADsMembers.get__NewEnum
title: IADsMembers::get__NewEnum
author: windows-sdk-content
description: The IADsMembers::get__NewEnum method gets a dependent enumerator object that implements IEnumVARIANT for this ADSI collection object. Be aware that there are two underscore characters in the function name (get__NewEnum).
old-location: adsi\iadsmembers_get__newenum.htm
tech.root: ADSI
ms.assetid: 5a65794c-2407-4267-bc02-d84a134f6bf4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsMembers interface [ADSI],get__NewEnum method, IADsMembers.get__NewEnum, IADsMembers::get__NewEnum, _ds_iadsmembers_get__newenum, adsi.iadsmembers__get____newenum, adsi.iadsmembers_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsMembers interface, iads/IADsMembers::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsMembers.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsMembers::get__NewEnum


## -description


The <b>IADsMembers::get__NewEnum</b> method gets a dependent enumerator object that implements  <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> for this ADSI collection object. Be aware that there are two underscore characters in the function name (<b>get__NewEnum</b>).


## -parameters




### -param ppEnumerator [out]

Pointer to a pointer to the <a href="_com_iunknown">IUnknown</a> interface on the enumerator object for this collection.


## -returns



This method supports the standard return values, including S_OK. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>



<a href="https://msdn.microsoft.com/ed4e98e5-053c-4d3b-bcd0-3add96bbe120">IADsMembers Property Methods</a>



<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="_com_iunknown">IUnknown</a>
 

 

