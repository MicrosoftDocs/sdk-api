---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

