---
UID: NF:adsprop.ADsPropGetInitInfo
title: ADsPropGetInitInfo function
author: windows-driver-content
description: Used to obtain directory object data that an Active Directory Domain Services property sheet extension applies to.
old-location: ad\adspropgetinitinfo.htm
old-project: AD
ms.assetid: dcc4ea8f-6924-4e26-a675-ce326f35933c
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: ADsPropGetInitInfo, ADsPropGetInitInfo function [Active Directory], ad.adspropgetinitinfo, adsprop/ADsPropGetInitInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: adsprop.h
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
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dsprop.dll
api_name:
-	ADsPropGetInitInfo
product: Windows
targetos: Windows
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
---

# ADsPropGetInitInfo function


## -description


The <b>ADsPropGetInitInfo</b> function is used to obtain directory object data that an Active Directory Domain Services property sheet extension applies to.


## -parameters




### -param hNotifyObj

TBD


### -param pInitParams [out]

Pointer to an <a href="https://msdn.microsoft.com/cbee3515-5037-4d65-8817-4c63fe13ef5d">ADSPROPINITPARAMS</a> structure that receives the directory object data. The <b>dwSize</b> member of this structure must be entered before calling this function.


#### - hNotifyObject [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


## -returns



Returns nonzero if successful or zero otherwise.




## -remarks



The memory  for the <b>pwzCN</b> and <b>pWritableAttrs</b> members is allocated by the <b>ADsPropGetInitInfo</b> function. This memory is freed by the system after all property sheet objects are destroyed. The reference count for the interface pointer in <b>pDsObj</b> is not incremented by calling <b>ADsPropGetInitInfo</b>, so the interface must not be released by the caller.

For multiple-selection property sheets, the system only binds to the first object in the <a href="https://msdn.microsoft.com/2f16a015-a777-4410-bed5-d409a4869c97">DSOBJECT</a> array. Because of this, <b>ADsPropGetInitInfo</b> only supplies the <a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a> and writable attributes for the first object in the array. The other objects in the array are not bound to.


#### Examples

The following code example shows how to use the <b>ADsPropGetInitInfo</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT GetADsPageInfo(HWND hwndNotifyObject, ADSPROPINITPARAMS *pip)
{
    if((NULL == pip) || (!IsWindow(hwndNotifyObject)))
    {
        return E_INVALIDARG;
    }

    ADSPROPINITPARAMS   InitParams;
    
    InitParams.dwSize = sizeof(ADSPROPINITPARAMS);
    if(ADsPropGetInitInfo(hwndNotifyObject, &amp;InitParams))
    {
        *pip = InitParams;
    
        return InitParams.hr;
    }
    
    return E_FAIL;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cbee3515-5037-4d65-8817-4c63fe13ef5d">ADSPROPINITPARAMS</a>



<a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>
 

 

