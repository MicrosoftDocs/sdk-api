---
UID: NF:shlobj_core.SHHandleUpdateImage
title: SHHandleUpdateImage function
author: windows-driver-content
description: SHHandleUpdateImage may be altered or unavailable.
old-location: shell\SHHandleUpdateImage.htm
old-project: shell
ms.assetid: 9d43e28a-bce0-4da4-98c9-5a6a199b4d8e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: SHHandleUpdateImage, SHHandleUpdateImage function [Windows Shell], _win32_SHHandleUpdateImage, shell.SHHandleUpdateImage, shlobj_core/SHHandleUpdateImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	SHHandleUpdateImage
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHHandleUpdateImage function


## -description


<p class="CCE_Message">[<b>SHHandleUpdateImage</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Handles the <b>SHCNE_UPDATEIMAGE</b> Shell change notification.


## -parameters




### -param pidlExtra [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The index in the system image list that has changed, specified in the <i>pidl2</i> parameter of <a href="https://msdn.microsoft.com/27ef6a2e-e463-4ba7-922f-20bf8e118d3a">IShellChangeNotify::OnChange</a>.


## -returns



Type: <b>int</b>

Returns -1 on failure or the index of the changed image list entry on success.




## -remarks



Use <b>SHHandleUpdateImage</b> only when the <i>pidl2</i> parameter received by your change notification callback is non-<b>NULL</b>.
            


#### Examples

The following example demonstrates the use of <b>SHHandleUpdateImage</b> in the implementation of <a href="https://msdn.microsoft.com/27ef6a2e-e463-4ba7-922f-20bf8e118d3a">IShellChangeNotify::OnChange</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyShellChangeNotify::OnChange(LONG lEvent, 
                                            LPCITEMIDLIST pidl1, 
                                            LPCITEMIDLIST pidl2)
{
    HRESULT hr = E_FAIL;
    int iImage;

    switch(lEvent)
    {
        // An image in the system image list has changed.
        case SHCNE_UPDATEIMAGE:
        {
            hr = S_OK;

            if (pidl2)
                iImage = SHHandleUpdateImage(pidl2);
            else
                iImage = *(int UNALIGNED *)((BYTE *)pidl1 + 2);
               
            if (iImage != -1)
            {
                // Process iImage as desired.
            }
            break;
        }
        // Other cases
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fc8d0bdd-0ca5-40e3-bdad-68ca1c64b08e">IShellChangeNotify</a>



<a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a>
 

 

