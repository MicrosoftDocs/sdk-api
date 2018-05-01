---
UID: NF:mswmdm.IWMDMStorageGlobals.GetSerialNumber
title: IWMDMStorageGlobals::GetSerialNumber method
author: windows-driver-content
description: The GetSerialNumber method retrieves a serial number that uniquely identifies the storage medium.
old-location: wmdm\iwmdmstorageglobals_getserialnumber.htm
old-project: WMDM
ms.assetid: 13783d0e-82e6-4340-bb06-85b8d3d06b5c
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetSerialNumber method [windows Media Device Manager], GetSerialNumber method [windows Media Device Manager], IWMDMStorageGlobals interface, GetSerialNumber,IWMDMStorageGlobals.GetSerialNumber, IWMDMStorageGlobals, IWMDMStorageGlobals interface [windows Media Device Manager], GetSerialNumber method, IWMDMStorageGlobals::GetSerialNumber, IWMDMStorageGlobalsGetSerialNumber, mswmdm/IWMDMStorageGlobals::GetSerialNumber, wmdm.iwmdmstorageglobals_getserialnumber
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMStorageGlobals.GetSerialNumber
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDMStorageGlobals::GetSerialNumber method


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
 

 

