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

# WlanSetInterface function


## -description


The <b>WlanSetInterface</b> function sets user-configurable parameters for a specified interface.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of the interface to be configured.


### -param OpCode [in]

A <a href="https://msdn.microsoft.com/4f68e52b-7fa3-4654-b4d3-41ca627c138a">WLAN_INTF_OPCODE</a> value that specifies the parameter to be set.  The following table lists the valid constants along with the data type of the parameter in <i>pData</i>.

<table>
<tr>
<th><b>WLAN_INTF_OPCODE</b> value</th>
<th><i>pData</i> data type</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_autoconf_enabled</b>

</td>
<td><b>BOOL</b></td>
<td>
Enables or disables auto config for the indicated interface.

</td>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_background_scan_enabled</b>

</td>
<td><b>BOOL</b></td>
<td>
Enables or disables background scan for the indicated interface.

</td>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_radio_state</b>

</td>
<td>
<a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a>
</td>
<td>
Sets the software radio state of a specific physical layer (PHY) for the interface.

</td>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_bss_type</b>

</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff547669">DOT11_BSS_TYPE</a>
</td>
<td>
Sets the BSS type.

</td>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_media_streaming_mode</b>

</td>
<td><b>BOOL</b></td>
<td>
Sets media streaming mode for the driver.

</td>
</tr>
<tr>
<td>
<b>wlan_intf_opcode_current_operation_mode</b>

</td>
<td><b>ULONG</b></td>
<td>
Sets the current operation mode for the interface. For more information, see Remarks.

</td>
</tr>
</table>
 

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_intf_opcode_autoconf_enabled</b> and <b>wlan_intf_opcode_bss_type</b> constants are valid.


### -param dwDataSize [in]

The size of the <i>pData</i> parameter, in bytes. If <i>dwDataSize</i> is larger than the actual amount of memory allocated to <i>pData</i>, then an access violation will occur in the calling program.


### -param pData [in]

The value to be set as specified by the <i>OpCode</i> parameter. The type of data pointed to by <i>pData</i> must be appropriate for the specified <i>OpCode</i>. Use the table above to determine the type of data to use.

<div class="alert"><b>Note</b>  If <i>OpCode</i> is set to <b>wlan_intf_opcode_autoconf_enabled</b>, <b>wlan_intf_opcode_background_scan_enabled</b>, or <b>wlan_intf_opcode_media_streaming_mode</b>, then <i>pData</i> may point to an integer value. If <i>pData</i> points to 0, then the value is converted to <b>FALSE</b>. If <i>pData</i> points to a nonzero integer, then the value is converted to <b>TRUE</b>. </div>
<div> </div>

### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.




## -remarks



When   <i>OpCode</i> is set to  <b>wlan_intf_opcode_current_operation_mode</b>,  the <b>WlanSetInterface</b>  function sets the current operation mode of the wireless interface. For more information about operation modes, see <a href="http://go.microsoft.com/fwlink/p/?linkid=71672">Native 802.11 Operation Modes</a>. Two operation modes are supported: <b>DOT11_OPERATION_MODE_EXTENSIBLE_STATION</b> and  <b>DOT11_OPERATION_MODE_NETWORK_MONITOR</b>. The operation mode constants are defined in the header file Windot11.h. If <i>pData</i> does not point to one of these values when <i>OpCode</i> is set to  <b>wlan_intf_opcode_current_operation_mode</b>, the  <b>WlanSetInterface</b>   function will fail with an error.

To enable or disable the automatic configuration service   at the command line, which is functionally equivalent to calling <b>WlanSetInterface</b> with  <i>OpCode</i> set to  <b>wlan_intf_opcode_autoconf_enabled</b>, use the <b>netsh wlan setautoconfig</b> command. For more information, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=120964">Netsh Commands for Wireless Local Area Network (wlan)</a>. 

The software radio state can be changed by calling the <b>WlanSetInterface</b> function.   The hardware radio state cannot be changed by calling the <b>WlanSetInterface</b> function.  When the <i>OpCode</i> parameter is set to <b>wlan_intf_opcode_radio_state</b>,  the <b>WlanSetInterface</b> function sets the software radio state of a specific PHY. The <i>pData</i> parameter must point to a <a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a> structure with the new radio state values to use. The <b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure is ignored when  the <b>WlanSetInterface</b> function is called with the <i>OpCode</i> parameter set to <b>wlan_intf_opcode_radio_state</b> and the <i>pData</i> parameter points to a <b>WLAN_PHY_RADIO_STATE</b> structure. The radio state of a PHY is off if either the software radio state (<b>dot11SoftwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure) or the hardware radio state (<b>dot11HardwareRadioState</b> member of the <b>WLAN_PHY_RADIO_STATE</b> structure) is off.  

Changing the software radio state of a physical network interface could cause related changes in the state of the wireless Hosted Network or virtual wireless adapter radio states. The PHYs of every virtual wireless adapter are linked. For more information, see the <a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>.




## -see-also




<a href="https://msdn.microsoft.com/a6990759-9b84-4644-8f82-75aa63e8197b">About the Wireless Hosted Network</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547669">DOT11_BSS_TYPE</a>



<a href="https://msdn.microsoft.com/4f68e52b-7fa3-4654-b4d3-41ca627c138a">WLAN_INTF_OPCODE</a>



<a href="https://msdn.microsoft.com/20da1494-4264-4d0d-b789-25e2be6a8dd4">WLAN_PHY_RADIO_STATE</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

