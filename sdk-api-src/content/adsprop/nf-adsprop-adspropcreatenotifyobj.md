---
UID: NF:adsprop.ADsPropCreateNotifyObj
title: ADsPropCreateNotifyObj function
author: windows-sdk-content
description: The ADsPropCreateNotifyObj function is used to create, or obtain, a notification object for use by an Active Directory Domain Services property sheet extension.
old-location: ad\adspropcreatenotifyobj.htm
tech.root: ad
ms.assetid: bfca3801-0d24-4177-8173-b6bf4b854fae
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ADsPropCreateNotifyObj, ADsPropCreateNotifyObj function [Active Directory], ad.adspropcreatenotifyobj, adsprop/ADsPropCreateNotifyObj
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
req.lib: Dsprop.lib
req.dll: Dsprop.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dsprop.dll
api_name:
 - ADsPropCreateNotifyObj
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ADsPropCreateNotifyObj function


## -description


The <b>ADsPropCreateNotifyObj</b> function is used to create, or obtain, a notification object for use by an Active Directory Domain Services property sheet extension.


## -parameters




### -param pAppThdDataObj [in]

A pointer to the <a href="_ole_idataobject">IDataObject</a> object that represents the directory object that the property page applies to. This is the <b>IDataObject</b> passed to the property page <a href="_win32_ishellextinit_win32_ishellextinit_initialize_cpp">IShellExtInit::Initialize</a> method.


### -param pwzADsObjName [in]

The Active Directory Domain Services object name obtained by calling the <a href="_ole_idataobject_getdata">IDataObject::GetData</a> method for the <a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a> clipboard format on the <a href="_ole_idataobject">IDataObject</a> represented by <i>pAppThdDataObj</i>.


### -param phNotifyObj [out]

Pointer to an <b>HWND</b> value that receives the handle of the notification object.


## -returns



Returns <b>S_OK</b> if successful, or an OLE-defined error value otherwise.




## -remarks



The <b>ADsPropCreateNotifyObj</b> function is used in the implementation of an Active Directory Domain Services property sheet extension. The extension must first request the  <a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a> data from the <a href="_ole_idataobject">IDataObject</a> interface passed to <a href="_win32_ishellextinit_win32_ishellextinit_initialize_cpp">IShellExtInit::Initialize</a> by calling <a href="_ole_idataobject_getdata">IDataObject::GetData</a>. This provides the data object and object name required to call <b>ADsPropCreateNotifyObj</b>.

When the notification object is no longer required, a <a href="https://msdn.microsoft.com/b0f58c73-8953-412d-b801-bf34967fe0b4">WM_ADSPROP_NOTIFY_EXIT</a> message is sent to the notification object. This causes the notification object to destroy itself. When the <b>WM_ADSPROP_NOTIFY_EXIT</b> message is sent, the notification object handle should be considered invalid.


#### Examples

The following C++ example shows how to use the <b>ADsPropCreateNotifyObj</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HWND CreateADsNotificationObject(IDataObject *pDataObject)
{
    STGMEDIUM   stm;
    FORMATETC   fe;
    HRESULT     hr;
    HWND        hwndNotifyObject = NULL;

    if(NULL == pDataObject)
    {
        return NULL;
    }

    fe.cfFormat = RegisterClipboardFormat(CFSTR_DSOBJECTNAMES);
    if(0 == fe.cfFormat)
    {
        return NULL;
    }
    fe.ptd = NULL;
    fe.dwAspect = DVASPECT_CONTENT;
    fe.lindex = -1;
    fe.tymed = TYMED_HGLOBAL;
    hr = pDataObject-&gt;GetData(&amp;fe, &amp;stm);
    if(SUCCEEDED(hr))
    {
        LPDSOBJECTNAMES pdson = 
            (LPDSOBJECTNAMES)GlobalLock(stm.hGlobal);

        if(pdson)
        {
            LPWSTR  pwszName = (LPWSTR)((LPBYTE)pdson + 
                pdson-&gt;aObjects[0].offsetName);
            
            hr = ADsPropCreateNotifyObj(pDataObject, 
                pwszName, 
                &amp;hwndNotifyObject);
    
            GlobalUnlock(stm.hGlobal);    
        }
        
        ReleaseStgMedium(&amp;stm);
    }

    return hwndNotifyObject;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9be96d2a-6545-4986-b47b-1eab6a02ac26">CFSTR_DSOBJECTNAMES</a>



<a href="_ole_idataobject">IDataObject</a>



<a href="_ole_idataobject_getdata">IDataObject::GetData</a>



<a href="_win32_ishellpropsheetext_win32_ishellpropsheetext_addpages_cpp">IShellPropSheetExt::AddPages</a>



<a href="https://msdn.microsoft.com/b0f58c73-8953-412d-b801-bf34967fe0b4">WM_ADSPROP_NOTIFY_EXIT</a>
 

 

