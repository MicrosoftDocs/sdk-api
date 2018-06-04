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

# IWMDMStorageGlobals::GetSerialNumber


## -description



The <b>GetSerialNumber</b> method retrieves a serial number that uniquely identifies the storage medium.




## -parameters




### -param pSerialNum [out]

Pointer to a <a href="https://msdn.microsoft.com/eaa5786e-a2a1-42d7-b527-be83d944cb20">WMDMID</a> structure specifying the serial number information.


### -param abMac [in, out]

Array of bytes specifying the message authentication code for the parameter data of this method. This memory is allocated and freed by the caller.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Not all storage media support serial numbers, but a serial number is required to support Microsoft digital rights management. If the storage medium cannot report a unique serial number, content protected by Microsoft digital rights management cannot be transferred to this storage medium. The return code should be checked to determine whether the storage medium provides this support.


#### Examples

The following C++ code retrieves the serial number of the root storage object, and verifies the MAC.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    hr = m_pStorageGlobals-&gt;GetSerialNumber(&amp;m_SerialNumber, (BYTE*)abMAC);
    if (SUCCEEDED(hr))
    {
        // Verify the MAC using the CSecureChannelClient member.
        m_pSAC-&gt;MACInit(&amp;hMAC);
        m_pSAC-&gt;MACUpdate(hMAC, (BYTE*)(&amp;m_SerialNumber), sizeof(m_SerialNumber));
        m_pSAC-&gt;MACFinal(hMAC, (BYTE*)abMACVerify);
        if (memcmp(abMACVerify, abMAC, sizeof(abMAC)) != 0)
        {
            hr = E_FAIL;
        }
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

