---
UID: TP:appxpkg
ms.assetid: 293875dc-2153-3c83-b216-e0140d6681e4
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Packaging, deployment, and query of Windows Store apps



Overview of the Packaging, deployment, and query of Windows Store apps technology.

To develop Packaging, deployment, and query of Windows Store apps, you need these headers:

 * [appmodel.h](..\appmodel\index.md)
 * [appxpackaging.h](..\appxpackaging\index.md)

For the programming guide, see [Packaging, deployment, and query of Windows Store apps](https://review.docs.microsoft.com/en-us/win32-test/appxpkg).

## Functions

| Title   | Description   |
| ---- |:---- |
| [ClosePackageInfo function](..\appmodel\nf-appmodel-closepackageinfo.md) | Closes a reference to the specified package information. |
| [FindPackagesByPackageFamily function](..\appmodel\nf-appmodel-findpackagesbypackagefamily.md) | Finds the packages with the specified family name for the current user. |
| [FormatApplicationUserModelId function](..\appmodel\nf-appmodel-formatapplicationusermodelid.md) | Constructs an application user model ID from the package family name and the package relative application ID (PRAID). |
| [GetApplicationUserModelId function](..\appmodel\nf-appmodel-getapplicationusermodelid.md) | Gets the application user model ID for the specified process. |
| [GetApplicationUserModelIdFromToken function](..\appmodel\nf-appmodel-getapplicationusermodelidfromtoken.md) | Gets the application user model ID for the specified token. |
| [GetCurrentApplicationUserModelId function](..\appmodel\nf-appmodel-getcurrentapplicationusermodelid.md) | Gets the application user model ID for the current process. |
| [GetCurrentPackageFamilyName function](..\appmodel\nf-appmodel-getcurrentpackagefamilyname.md) | Gets the package family name for the calling process. |
| [GetCurrentPackageFullName function](..\appmodel\nf-appmodel-getcurrentpackagefullname.md) | Gets the package full name for the calling process. |
| [GetCurrentPackageId function](..\appmodel\nf-appmodel-getcurrentpackageid.md) | Gets the package identifier (ID) for the calling process. |
| [GetCurrentPackageInfo function](..\appmodel\nf-appmodel-getcurrentpackageinfo.md) | Gets the package information for the calling process. |
| [GetCurrentPackagePath function](..\appmodel\nf-appmodel-getcurrentpackagepath.md) | Gets the package path for the calling process. |
| [GetPackageApplicationIds function](..\appmodel\nf-appmodel-getpackageapplicationids.md) | Gets the IDs of apps in the specified package. |
| [GetPackageFamilyName function](..\appmodel\nf-appmodel-getpackagefamilyname.md) | Gets the package family name for the specified process. |
| [GetPackageFamilyNameFromToken function](..\appmodel\nf-appmodel-getpackagefamilynamefromtoken.md) | Gets the package family name for the specified token. |
| [GetPackageFullName function](..\appmodel\nf-appmodel-getpackagefullname.md) | Gets the package full name for the specified process. |
| [GetPackageFullNameFromToken function](..\appmodel\nf-appmodel-getpackagefullnamefromtoken.md) | Gets the package full name for the specified token. |
| [GetPackageId function](..\appmodel\nf-appmodel-getpackageid.md) | Gets the package identifier (ID) for the specified process. |
| [GetPackageInfo function](..\appmodel\nf-appmodel-getpackageinfo.md) | Gets the package information for the specified package. |
| [GetPackagePath function](..\appmodel\nf-appmodel-getpackagepath.md) | Gets the path for the specified package. |
| [GetPackagePathByFullName function](..\appmodel\nf-appmodel-getpackagepathbyfullname.md) | Gets the path of the specified package. |
| [GetPackagesByPackageFamily function](..\appmodel\nf-appmodel-getpackagesbypackagefamily.md) | Gets the packages with the specified family name for the current user. |
| [GetStagedPackageOrigin function](..\appmodel\nf-appmodel-getstagedpackageorigin.md) | Gets the origin of the specified package. |
| [GetStagedPackagePathByFullName function](..\appmodel\nf-appmodel-getstagedpackagepathbyfullname.md) | Gets the path of the specified staged package. |
| [OpenPackageInfoByFullName function](..\appmodel\nf-appmodel-openpackageinfobyfullname.md) | Opens the package information of the specified package. |
| [PackageFamilyNameFromFullName function](..\appmodel\nf-appmodel-packagefamilynamefromfullname.md) | Gets the package family name for the specified package full name. |
| [PackageFamilyNameFromId function](..\appmodel\nf-appmodel-packagefamilynamefromid.md) | Gets the package family name for the specified package identifier. |
| [PackageFullNameFromId function](..\appmodel\nf-appmodel-packagefullnamefromid.md) | Gets the package full name for the specified package identifier (ID). |
| [PackageIdFromFullName function](..\appmodel\nf-appmodel-packageidfromfullname.md) | Gets the package identifier (ID) for the specified package full name. |
| [PackageNameAndPublisherIdFromFamilyName function](..\appmodel\nf-appmodel-packagenameandpublisheridfromfamilyname.md) | Gets the package name and publisher identifier (ID) for the specified package family name. |
| [ParseApplicationUserModelId function](..\appmodel\nf-appmodel-parseapplicationusermodelid.md) | Deconstructs an application user model ID to its package family name and package relative application ID (PRAID). |

## Structures

| Title   | Description   |
| ---- |:---- |
| [APPX_ENCRYPTED_EXEMPTIONS structure](..\appxpackaging\ns-appxpackaging-appx_encrypted_exemptions.md) | Files exempted from Windows app package encryption. |
| [APPX_ENCRYPTED_PACKAGE_SETTINGS structure](..\appxpackaging\ns-appxpackaging-appx_encrypted_package_settings.md) | Settings for encrypted Windows app packages. |
| [APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure](..\appxpackaging\ns-appxpackaging-appx_encrypted_package_settings2.md) | Encrypted Windows app package settings. |
| [APPX_KEY_INFO structure](..\appxpackaging\ns-appxpackaging-appx_key_info.md) | Windows app package key information. |
| [APPX_PACKAGE_SETTINGS structure](..\appxpackaging\ns-appxpackaging-appx_package_settings.md) | Represents package settings used to create a package. |
| [APPX_PACKAGE_WRITER_PAYLOAD_STREAM structure](..\appxpackaging\ns-appxpackaging-appx_package_writer_payload_stream.md) | Contains the data and metadata of files to write into the app package. |
| [PACKAGE_ID structure](..\appmodel\ns-appmodel-package_id.md) | Represents package identification information, such as name, version, and publisher. |
| [PACKAGE_INFO structure](..\appmodel\ns-appmodel-package_info.md) | Represents package identification information that includes the package identifier, full name, and install location. |
| [PACKAGE_VERSION structure](..\appmodel\ns-appmodel-package_version.md) | Represents the package version information. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [APPX_BUNDLE_FOOTPRINT_FILE_TYPE enumeration](..\appxpackaging\ne-appxpackaging-appx_bundle_footprint_file_type.md) | Specifies the type of footprint file in a bundle. |
| [APPX_BUNDLE_PAYLOAD_PACKAGE_TYPE enumeration](..\appxpackaging\ne-appxpackaging-appx_bundle_payload_package_type.md) | Specifies the type of package for a IAppxBundleManifestPackageInfo object. |
| [APPX_CAPABILITIES enumeration](..\appxpackaging\ne-appxpackaging-appx_capabilities.md) | Specifies the capabilities or privileges requested by a package. |
| [APPX_COMPRESSION_OPTION enumeration](..\appxpackaging\ne-appxpackaging-appx_compression_option.md) | Specifies the degree of compression used to store the file in the package. |
| [APPX_ENCRYPTED_PACKAGE_OPTIONS enumeration](..\appxpackaging\ne-appxpackaging-appx_encrypted_package_options.md) | Encrypted app package options. |
| [APPX_FOOTPRINT_FILE_TYPE enumeration](..\appxpackaging\ne-appxpackaging-appx_footprint_file_type.md) | Specifies the type of footprint file in a package. |
| [APPX_PACKAGE_ARCHITECTURE enumeration](..\appxpackaging\ne-appxpackaging-appx_package_architecture.md) | Specifies the processor architectures supported by a package. |
| [APPX_PACKAGE_ARCHITECTURE2 enumeration](..\appxpackaging\ne-appxpackaging-appx_package_architecture2.md) | Specifies the processor architectures supported by a package. |
| [APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_MANIFEST_OPTIONS enumeration](..\appxpackaging\ne-appxpackaging-appx_package_editor_update_package_manifest_options.md) | Options for app manifest validation when updating the manifest. |
| [APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION enumeration](..\appxpackaging\ne-appxpackaging-appx_package_editor_update_package_option.md) | Options to use when updating an app package. |
| [PackageOrigin enumeration](..\appmodel\ne-appmodel-packageorigin.md) | Specifies the origin of a package. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IAppxBlockMapBlock interface](..\appxpackaging\nn-appxpackaging-iappxblockmapblock.md) | The IAppxBlockMapBlock interface provides a read-only object that represents an individual block within a file contained in the block map file (AppxBlockMap.xml) for the App package. |
| [IAppxBlockMapBlocksEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxblockmapblocksenumerator.md) | Enumerates the blocks from a block map in a single file. |
| [IAppxBlockMapFile interface](..\appxpackaging\nn-appxpackaging-iappxblockmapfile.md) | Represents a file in the block map. |
| [IAppxBlockMapFilesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxblockmapfilesenumerator.md) | Enumerates the files from a block map. |
| [IAppxBlockMapReader interface](..\appxpackaging\nn-appxpackaging-iappxblockmapreader.md) | Represents a read-only object model for block maps that provides access to the file attributes and block hashes. |
| [IAppxBundleFactory interface](..\appxpackaging\nn-appxpackaging-iappxbundlefactory.md) | Creates objects for reading and writing bundle packages. |
| [IAppxBundleManifestOptionalBundleInfo interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestoptionalbundleinfo.md) | Provides a read-only object model for an &lt;OptionalBundle&gt; element in a bundle package manifest. |
| [IAppxBundleManifestOptionalBundleInfoEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator.md) | Enumerates the optional bundle information from a bundle. |
| [IAppxBundleManifestPackageInfo interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestpackageinfo.md) | Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest. |
| [IAppxBundleManifestPackageInfo2 interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestpackageinfo2.md) | Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest. |
| [IAppxBundleManifestPackageInfoEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestpackageinfoenumerator.md) | Provides a read-only object model for the list of payload packages that are described in a bundle package manifest. |
| [IAppxBundleManifestReader interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestreader.md) | Provides a read-only object model for manifests of bundle packages. |
| [IAppxBundleManifestReader2 interface](..\appxpackaging\nn-appxpackaging-iappxbundlemanifestreader2.md) | Provides a read-only object model for manifests of bundle packages. |
| [IAppxBundleReader interface](..\appxpackaging\nn-appxpackaging-iappxbundlereader.md) | Provides a read-only object model for bundle packages. |
| [IAppxBundleWriter interface](..\appxpackaging\nn-appxpackaging-iappxbundlewriter.md) | Provides a write-only object model for bundle packages. |
| [IAppxBundleWriter2 interface](..\appxpackaging\nn-appxpackaging-iappxbundlewriter2.md) | Provides a write-only object model for bundle packages. |
| [IAppxBundleWriter3 interface](..\appxpackaging\nn-appxpackaging-iappxbundlewriter3.md) | Provides a write-only object model for bundle packages. |
| [IAppxBundleWriter4 interface](..\appxpackaging\nn-appxpackaging-iappxbundlewriter4.md) | Provides a write-only object model for bundle packages. |
| [IAppxContentGroup interface](..\appxpackaging\nn-appxpackaging-iappxcontentgroup.md) | Retrieves information about a content group. |
| [IAppxContentGroupFilesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxcontentgroupfilesenumerator.md) | Enumerates files in content groups from a content group map. |
| [IAppxContentGroupMapReader interface](..\appxpackaging\nn-appxpackaging-iappxcontentgroupmapreader.md) | Gets information about a content group map. |
| [IAppxContentGroupMapWriter interface](..\appxpackaging\nn-appxpackaging-iappxcontentgroupmapwriter.md) | Provides a write-only object model for a content group map. |
| [IAppxContentGroupsEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxcontentgroupsenumerator.md) | Enumerates the content groups from a content group map. |
| [IAppxEncryptedBundleWriter interface](..\appxpackaging\nn-appxpackaging-iappxencryptedbundlewriter.md) | Provides a write-only object model for encrypted bundle packages. |
| [IAppxEncryptedBundleWriter2 interface](..\appxpackaging\nn-appxpackaging-iappxencryptedbundlewriter2.md) | Provides a write-only object model for encrypted bundle packages. |
| [IAppxEncryptedBundleWriter3 interface](..\appxpackaging\nn-appxpackaging-iappxencryptedbundlewriter3.md) | Provides a write-only object model for encrypted bundle packages. |
| [IAppxEncryptedPackageWriter interface](..\appxpackaging\nn-appxpackaging-iappxencryptedpackagewriter.md) | Provides a write-only object model for encrypted app packages. |
| [IAppxEncryptedPackageWriter2 interface](..\appxpackaging\nn-appxpackaging-iappxencryptedpackagewriter2.md) | Provides a write-only object model for encrypted app packages. |
| [IAppxEncryptionFactory interface](..\appxpackaging\nn-appxpackaging-iappxencryptionfactory.md) | Creates objects for encrypting, decrypting, reading, and writing packages and bundles. |
| [IAppxEncryptionFactory2 interface](..\appxpackaging\nn-appxpackaging-iappxencryptionfactory2.md) | Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles. |
| [IAppxEncryptionFactory3 interface](..\appxpackaging\nn-appxpackaging-iappxencryptionfactory3.md) | Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles. |
| [IAppxEncryptionFactory4 interface](..\appxpackaging\nn-appxpackaging-iappxencryptionfactory4.md) | Creates objects for encrypting Windows app packages and bundles. |
| [IAppxFactory interface](..\appxpackaging\nn-appxpackaging-iappxfactory.md) | Creates objects for reading and writing app packages. |
| [IAppxFactory2 interface](..\appxpackaging\nn-appxpackaging-iappxfactory2.md) | Creates objects for reading and writing app packages. |
| [IAppxFile interface](..\appxpackaging\nn-appxpackaging-iappxfile.md) | Retrieves information about a payload or footprint file in a package. |
| [IAppxFilesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxfilesenumerator.md) | Enumerates the payload files in a package. |
| [IAppxManifestApplication interface](..\appxpackaging\nn-appxpackaging-iappxmanifestapplication.md) | Provides access to attribute values of the application. |
| [IAppxManifestApplicationsEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxmanifestapplicationsenumerator.md) | Enumerates the applications defined in the package manifest. |
| [IAppxManifestDeviceCapabilitiesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxmanifestdevicecapabilitiesenumerator.md) | Enumerates the device capabilities defined in the package manifest. |
| [IAppxManifestMainPackageDependenciesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxmanifestmainpackagedependenciesenumerator.md) | Enumerates &lt;MainPackageDependency&gt; elements from an app manifest. |
| [IAppxManifestMainPackageDependency interface](..\appxpackaging\nn-appxpackaging-iappxmanifestmainpackagedependency.md) | Provides access to attribute values of the main package dependency. |
| [IAppxManifestOptionalPackageInfo interface](..\appxpackaging\nn-appxpackaging-iappxmanifestoptionalpackageinfo.md) | Provides access to attribute values of the optional package information. |
| [IAppxManifestPackageDependenciesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxmanifestpackagedependenciesenumerator.md) | Enumerates the package dependencies defined in the package manifest. |
| [IAppxManifestPackageDependency interface](..\appxpackaging\nn-appxpackaging-iappxmanifestpackagedependency.md) | Describes the dependency of one package on another package. |
| [IAppxManifestPackageDependency2 interface](..\appxpackaging\nn-appxpackaging-iappxmanifestpackagedependency2.md) | Describes the dependency of one package on another package. |
| [IAppxManifestPackageId interface](..\appxpackaging\nn-appxpackaging-iappxmanifestpackageid.md) | Provides access to the package identity. |
| [IAppxManifestPackageId2 interface](..\appxpackaging\nn-appxpackaging-iappxmanifestpackageid2.md) | Provides access to the app package identity. |
| [IAppxManifestProperties interface](..\appxpackaging\nn-appxpackaging-iappxmanifestproperties.md) | Provides read-only access to the properties section of a package manifest. |
| [IAppxManifestReader interface](..\appxpackaging\nn-appxpackaging-iappxmanifestreader.md) | Represents an object model of the package manifest that provides methods to access manifest elements and attributes. |
| [IAppxManifestReader2 interface](..\appxpackaging\nn-appxpackaging-iappxmanifestreader2.md) | Represents an object model of the package manifest that provides methods to access manifest elements and attributes. |
| [IAppxManifestReader5 interface](..\appxpackaging\nn-appxpackaging-iappxmanifestreader5.md) | Represents an object model of the package manifest that provides methods to access manifest elements and attributes. |
| [IAppxManifestReader6 interface](..\appxpackaging\nn-appxpackaging-iappxmanifestreader6.md) | Represents an object model of the package manifest that provides methods to access manifest elements and attributes. |
| [IAppxManifestResourcesEnumerator interface](..\appxpackaging\nn-appxpackaging-iappxmanifestresourcesenumerator.md) | Enumerates the resources defined in the package manifest. |
| [IAppxManifestTargetDeviceFamily interface](..\appxpackaging\nn-appxpackaging-iappxmanifesttargetdevicefamily.md) | Retrieves information about the target device family from the AppxManifest.xml. |
| [IAppxPackageEditor interface](..\appxpackaging\nn-appxpackaging-iappxpackageeditor.md) | Provides functionality to edit app packages. |
| [IAppxPackageReader interface](..\appxpackaging\nn-appxpackaging-iappxpackagereader.md) | Provides a read-only object model for app packages. |
| [IAppxPackageReader2 interface](..\appxpackaging\nn-appxpackaging-iappxpackagereader2.md) | Provides a read-only object model for app packages. |
| [IAppxPackageWriter interface](..\appxpackaging\nn-appxpackaging-iappxpackagewriter.md) | Provides a write-only object model for app packages. |
| [IAppxPackageWriter2 interface](..\appxpackaging\nn-appxpackaging-iappxpackagewriter2.md) | Provides a write-only object model for app packages. |
| [IAppxPackageWriter3 interface](..\appxpackaging\nn-appxpackaging-iappxpackagewriter3.md) | Provides a write-only object model for app packages. |
| [IAppxSourceContentGroupMapReader interface](..\appxpackaging\nn-appxpackaging-iappxsourcecontentgroupmapreader.md) | Gets information about the source content group map. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IAppxBlockMapBlock::GetCompressedSize](..\appxpackaging\nf-appxpackaging-iappxblockmapblock-getcompressedsize.md) | Retrieves compressed size of the block. |
| [IAppxBlockMapBlock::GetHash](..\appxpackaging\nf-appxpackaging-iappxblockmapblock-gethash.md) | Retrieves the hash value of the block. |
| [IAppxBlockMapBlocksEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxblockmapblocksenumerator-getcurrent.md) | Gets the block at the current position of the enumerator. |
| [IAppxBlockMapBlocksEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxblockmapblocksenumerator-gethascurrent.md) | Determines whether there is a block at the current position of the enumerator. |
| [IAppxBlockMapBlocksEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxblockmapblocksenumerator-movenext.md) | Advances the position of the enumerator to the next block. |
| [IAppxBlockMapFile::GetBlocks](..\appxpackaging\nf-appxpackaging-iappxblockmapfile-getblocks.md) | Retrieves an enumerator for traversing the blocks of a file listed in the block map. |
| [IAppxBlockMapFile::GetLocalFileHeaderSize](..\appxpackaging\nf-appxpackaging-iappxblockmapfile-getlocalfileheadersize.md) | Retrieves the size of the zip local file header of the associated zip file item. |
| [IAppxBlockMapFile::GetName](..\appxpackaging\nf-appxpackaging-iappxblockmapfile-getname.md) | Retrieves the name of the associated zip file item. |
| [IAppxBlockMapFile::GetUncompressedSize](..\appxpackaging\nf-appxpackaging-iappxblockmapfile-getuncompressedsize.md) | Retrieves the uncompressed size of the associated zip file item. |
| [IAppxBlockMapFile::ValidateFileHash](..\appxpackaging\nf-appxpackaging-iappxblockmapfile-validatefilehash.md) | Validates the content of a file against the hashes stored in the block elements for this block map file. |
| [IAppxBlockMapFilesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxblockmapfilesenumerator-getcurrent.md) | Gets the file at the current position of the enumerator. |
| [IAppxBlockMapFilesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxblockmapfilesenumerator-gethascurrent.md) | Determines whether there is a file at the current position of the enumerator. |
| [IAppxBlockMapFilesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxblockmapfilesenumerator-movenext.md) | Advances the position of the enumerator to the next file. |
| [IAppxBlockMapReader::GetFile](..\appxpackaging\nf-appxpackaging-iappxblockmapreader-getfile.md) | Retrieves data corresponding to a file in the block map with the specified file name. |
| [IAppxBlockMapReader::GetFiles](..\appxpackaging\nf-appxpackaging-iappxblockmapreader-getfiles.md) | Retrieves an enumerator for traversing the files listed in the block map. |
| [IAppxBlockMapReader::GetHashMethod](..\appxpackaging\nf-appxpackaging-iappxblockmapreader-gethashmethod.md) | Retrieves the URI for the hash algorithm used to create block hashes in the block map. |
| [IAppxBlockMapReader::GetStream](..\appxpackaging\nf-appxpackaging-iappxblockmapreader-getstream.md) | Retrieves a read-only stream that represents the XML content of the block map. |
| [IAppxBundleFactory::CreateBundleManifestReader](..\appxpackaging\nf-appxpackaging-iappxbundlefactory-createbundlemanifestreader.md) | Creates a read-only bundle manifest object from a standalone stream to AppxBundleManifest.xml. |
| [IAppxBundleFactory::CreateBundleReader](..\appxpackaging\nf-appxpackaging-iappxbundlefactory-createbundlereader.md) | Creates a read-only bundle object that reads its contents from an IStream object. |
| [IAppxBundleFactory::CreateBundleWriter](..\appxpackaging\nf-appxpackaging-iappxbundlefactory-createbundlewriter.md) | Creates a write-only bundle object to which app packages can be added. |
| [IAppxBundleManifestOptionalBundleInfo::GetFileName](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfo-getfilename.md) | Retrieves the file-name attribute of the &lt;OptionalBundle&gt;. |
| [IAppxBundleManifestOptionalBundleInfo::GetPackageId](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfo-getpackageid.md) | Retrieves an object that represents the identity of the &lt;OptionalBundle&gt;. |
| [IAppxBundleManifestOptionalBundleInfo::GetPackageInfoItems](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfo-getpackageinfoitems.md) | Retrieves optional packages in the bundle. |
| [IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-getcurrent.md) | Gets the optional bundle information at the current position of the enumerator. |
| [IAppxBundleManifestOptionalBundleInfoEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-gethascurrent.md) | Determines whether there is optional bundle information at the current position of the enumerator. |
| [IAppxBundleManifestOptionalBundleInfoEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-movenext.md) | Advances the position of the enumerator to the next set of optional bundle information. |
| [IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo2-getisdefaultapplicablepackage.md) | Determines whether the app package is a default applicable package. |
| [IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo2-getisnonqualifiedresourcepackage.md) | Determines whether the app package is a non-qualified resource package. |
| [IAppxBundleManifestPackageInfo2::GetIsPackageReference](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo2-getispackagereference.md) | Determines whether a package is stored inside an app bundle, or if it's a reference to a package. |
| [IAppxBundleManifestPackageInfo::GetFileName](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getfilename.md) | Retrieves the file-name attribute of the package. |
| [IAppxBundleManifestPackageInfo::GetOffset](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getoffset.md) | Retrieves the offset of the package relative to the beginning of the bundle. |
| [IAppxBundleManifestPackageInfo::GetPackageId](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getpackageid.md) | Retrieves an object that represents the identity of the app package. |
| [IAppxBundleManifestPackageInfo::GetPackageType](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getpackagetype.md) | Retrieves the type of package that is represented by the package info. |
| [IAppxBundleManifestPackageInfo::GetResources](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getresources.md) | Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest. |
| [IAppxBundleManifestPackageInfo::GetSize](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfo-getsize.md) | Retrieves the size of the package, in bytes. |
| [IAppxBundleManifestPackageInfoEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfoenumerator-getcurrent.md) | Gets the &lt;Package&gt; element at the current position of the enumerator. |
| [IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfoenumerator-gethascurrent.md) | Determines whether there are more elements in the enumerator. |
| [IAppxBundleManifestPackageInfoEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestpackageinfoenumerator-movenext.md) | Advances the position of the enumerator to the next &lt;Package&gt; element. |
| [IAppxBundleManifestReader2::GetOptionalBundles](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestreader2-getoptionalbundles.md) | Retrieves an object that represents the &lt;OptionalBundles&gt; element under the root &lt;Bundle&gt; element. |
| [IAppxBundleManifestReader::GetPackageId](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestreader-getpackageid.md) | Retrieves an object that represents the &lt;Identity&gt; element under the root &lt;Bundle&gt; element. |
| [IAppxBundleManifestReader::GetPackageInfoItems](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestreader-getpackageinfoitems.md) | Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element. |
| [IAppxBundleManifestReader::GetStream](..\appxpackaging\nf-appxpackaging-iappxbundlemanifestreader-getstream.md) | Gets the raw XML document without any preprocessing. |
| [IAppxBundleReader::GetBlockMap](..\appxpackaging\nf-appxpackaging-iappxbundlereader-getblockmap.md) | Retrieves a read-only block map object from the bundle. |
| [IAppxBundleReader::GetFootprintFile](..\appxpackaging\nf-appxpackaging-iappxbundlereader-getfootprintfile.md) | Retrieves the specified type of footprint file from the bundle. |
| [IAppxBundleReader::GetManifest](..\appxpackaging\nf-appxpackaging-iappxbundlereader-getmanifest.md) | Retrieves a read-only manifest object from the bundle. |
| [IAppxBundleReader::GetPayloadPackage](..\appxpackaging\nf-appxpackaging-iappxbundlereader-getpayloadpackage.md) | Retrieves an appx file object for the payload package with the specified file name. |
| [IAppxBundleReader::GetPayloadPackages](..\appxpackaging\nf-appxpackaging-iappxbundlereader-getpayloadpackages.md) | Retrieves an enumerator that iterates over the list of all payload packages in the bundle. |
| [IAppxBundleWriter2::AddExternalPackageReference](..\appxpackaging\nf-appxpackaging-iappxbundlewriter2-addexternalpackagereference.md) | Adds a reference to an external package to the package bundle. |
| [IAppxBundleWriter3::AddPackageReference](..\appxpackaging\nf-appxpackaging-iappxbundlewriter3-addpackagereference.md) | Adds a reference to an optional app package or a payload file within an app bundle. |
| [IAppxBundleWriter3::Close](..\appxpackaging\nf-appxpackaging-iappxbundlewriter3-close.md) | Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream. |
| [IAppxBundleWriter4::AddExternalPackageReference](..\appxpackaging\nf-appxpackaging-iappxbundlewriter4-addexternalpackagereference.md) | Adds a reference within the package bundle to an external app package. |
| [IAppxBundleWriter4::AddPackageReference](..\appxpackaging\nf-appxpackaging-iappxbundlewriter4-addpackagereference.md) | Adds a reference to an optional app package or a payload file within an app bundle. |
| [IAppxBundleWriter4::AddPayloadPackage](..\appxpackaging\nf-appxpackaging-iappxbundlewriter4-addpayloadpackage.md) | Adds a new app package to the bundle. |
| [IAppxBundleWriter::AddPayloadPackage](..\appxpackaging\nf-appxpackaging-iappxbundlewriter-addpayloadpackage.md) | Adds a new app package to the bundle. |
| [IAppxBundleWriter::Close](..\appxpackaging\nf-appxpackaging-iappxbundlewriter-close.md) | Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream. |
| [IAppxContentGroup::GetFiles](..\appxpackaging\nf-appxpackaging-iappxcontentgroup-getfiles.md) | Gets files from a content group. |
| [IAppxContentGroup::GetName](..\appxpackaging\nf-appxpackaging-iappxcontentgroup-getname.md) | Gets the name of the content group. |
| [IAppxContentGroupFilesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxcontentgroupfilesenumerator-getcurrent.md) | Gets the file from the content group at the current position of the enumerator. |
| [IAppxContentGroupFilesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxcontentgroupfilesenumerator-gethascurrent.md) | Determines whether there is a file at the current position of the enumerator. |
| [IAppxContentGroupFilesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxcontentgroupfilesenumerator-movenext.md) | Advances the position of the enumerator to the next file. |
| [IAppxContentGroupMapReader::GetAutomaticGroups](..\appxpackaging\nf-appxpackaging-iappxcontentgroupmapreader-getautomaticgroups.md) | Gets the automatic content group(s) from the content group map. |
| [IAppxContentGroupMapReader::GetRequiredGroup](..\appxpackaging\nf-appxpackaging-iappxcontentgroupmapreader-getrequiredgroup.md) | Gets the required content group from the content group map. |
| [IAppxContentGroupMapWriter::AddAutomaticFile](..\appxpackaging\nf-appxpackaging-iappxcontentgroupmapwriter-addautomaticfile.md) | Adds files to an automatic content group in a content group map. |
| [IAppxContentGroupMapWriter::AddAutomaticGroup](..\appxpackaging\nf-appxpackaging-iappxcontentgroupmapwriter-addautomaticgroup.md) | Adds an automatic content group to the content group map. |
| [IAppxContentGroupsEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxcontentgroupsenumerator-getcurrent.md) | Gets the content group at the current position of the enumerator. |
| [IAppxContentGroupsEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxcontentgroupsenumerator-gethascurrent.md) | Determines whether there is a content group at the current position of the enumerator. |
| [IAppxContentGroupsEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxcontentgroupsenumerator-movenext.md) | Advances the position of the enumerator to the next content group. |
| [IAppxEncryptedBundleWriter2::AddExternalPackageReference](..\appxpackaging\nf-appxpackaging-iappxencryptedbundlewriter2-addexternalpackagereference.md) | Adds a reference within the encrypted package bundle to an external app package. |
| [IAppxEncryptedBundleWriter3::AddExternalPackageReference](..\appxpackaging\nf-appxpackaging-iappxencryptedbundlewriter3-addexternalpackagereference.md) | Adds a reference within the encrypted package bundle to an external app package. |
| [IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted](..\appxpackaging\nf-appxpackaging-iappxencryptedbundlewriter3-addpayloadpackageencrypted.md) | Encrypts a new payload package to the bundle. |
| [IAppxEncryptedBundleWriter::AddPayloadPackageEncrypted](..\appxpackaging\nf-appxpackaging-iappxencryptedbundlewriter-addpayloadpackageencrypted.md) | Encrypts a new payload package to the bundle. |
| [IAppxEncryptedBundleWriter::Close](..\appxpackaging\nf-appxpackaging-iappxencryptedbundlewriter-close.md) | Writes the bundle manifest and blockmap footprint files to the bundle. |
| [IAppxEncryptedPackageWriter2::AddPayloadFilesEncrypted](..\appxpackaging\nf-appxpackaging-iappxencryptedpackagewriter2-addpayloadfilesencrypted.md) | Adds one or more payload files to an encrypted app package. |
| [IAppxEncryptedPackageWriter::AddPayloadFileEncrypted](..\appxpackaging\nf-appxpackaging-iappxencryptedpackagewriter-addpayloadfileencrypted.md) | Adds a new encrypted payload file to the appx package. |
| [IAppxEncryptedPackageWriter::Close](..\appxpackaging\nf-appxpackaging-iappxencryptedpackagewriter-close.md) | Closes and finalizes the written package stream. |
| [IAppxEncryptionFactory2::CreateEncryptedPackageWriter](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory2-createencryptedpackagewriter.md) | Creates a new instance of an IAppxEncryptedPackageWriter. |
| [IAppxEncryptionFactory3::CreateEncryptedBundleWriter](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory3-createencryptedbundlewriter.md) | Creates a write-only bundle object to which encrypted Windows app packages can be added. |
| [IAppxEncryptionFactory3::CreateEncryptedPackageWriter](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory3-createencryptedpackagewriter.md) | Creates a new instance of an IAppxEncryptedPackageWriter. |
| [IAppxEncryptionFactory3::EncryptBundle](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory3-encryptbundle.md) | Creates an encrypted Windows app bundle from an unencrypted one. |
| [IAppxEncryptionFactory3::EncryptPackage](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory3-encryptpackage.md) | Creates an encrypted Windows app package from an unencrypted one. |
| [IAppxEncryptionFactory4::EncryptPackage](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory4-encryptpackage.md) | Creates an encrypted Windows app package from an unencrypted one. |
| [IAppxEncryptionFactory::CreateEncryptedBundleReader](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-createencryptedbundlereader.md) | Creates a read-only bundle object to which encrypted Windows app packages can be added. |
| [IAppxEncryptionFactory::CreateEncryptedBundleWriter](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-createencryptedbundlewriter.md) | Creates a write-only bundle object to which encrypted Windows app packages can be added. |
| [IAppxEncryptionFactory::CreateEncryptedPackageReader](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-createencryptedpackagereader.md) | Creates a new instance of IAppxEncryptedPackageReader. |
| [IAppxEncryptionFactory::CreateEncryptedPackageWriter](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-createencryptedpackagewriter.md) | Creates a new instance of an IAppxEncryptedPackageWriter. |
| [IAppxEncryptionFactory::DecryptBundle](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-decryptbundle.md) | Creates an unencrypted Windows app bundle from an encrypted one. |
| [IAppxEncryptionFactory::DecryptPackage](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-decryptpackage.md) | Creates an unencrypted Windows app package from an encrypted one. |
| [IAppxEncryptionFactory::EncryptBundle](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-encryptbundle.md) | Creates an encrypted Windows app bundle from an unencrypted one. |
| [IAppxEncryptionFactory::EncryptPackage](..\appxpackaging\nf-appxpackaging-iappxencryptionfactory-encryptpackage.md) | Creates an encrypted Windows app package from an unencrypted one. |
| [IAppxFactory2::CreateContentGroupMapReader](..\appxpackaging\nf-appxpackaging-iappxfactory2-createcontentgroupmapreader.md) | Creates an IAppxContentGroupMapReader. |
| [IAppxFactory2::CreateContentGroupMapWriter](..\appxpackaging\nf-appxpackaging-iappxfactory2-createcontentgroupmapwriter.md) | Creates an IAppxContentGroupMapWriter. |
| [IAppxFactory2::CreateSourceContentGroupMapReader](..\appxpackaging\nf-appxpackaging-iappxfactory2-createsourcecontentgroupmapreader.md) | Creates an IAppxSourceContentGroupMapReader. |
| [IAppxFactory::CreateBlockMapReader](..\appxpackaging\nf-appxpackaging-iappxfactory-createblockmapreader.md) | Creates a read-only block map object model from contents provided by an IStream. |
| [IAppxFactory::CreateManifestReader](..\appxpackaging\nf-appxpackaging-iappxfactory-createmanifestreader.md) | Creates a read-only manifest object model from contents provided by an IStream. |
| [IAppxFactory::CreatePackageReader](..\appxpackaging\nf-appxpackaging-iappxfactory-createpackagereader.md) | Creates a read-only package reader from the contents provided by an IStream. This method does not validate the digital signature. |
| [IAppxFactory::CreatePackageWriter](..\appxpackaging\nf-appxpackaging-iappxfactory-createpackagewriter.md) | Creates a write-only package object to which files can be added. |
| [IAppxFactory::CreateValidatedBlockMapReader](..\appxpackaging\nf-appxpackaging-iappxfactory-createvalidatedblockmapreader.md) | Creates a read-only block map object model from contents provided by an IStream and a digital signature. |
| [IAppxFile::GetCompressionOption](..\appxpackaging\nf-appxpackaging-iappxfile-getcompressionoption.md) | Retrieves the compression option that is used to store the file in the package. |
| [IAppxFile::GetContentType](..\appxpackaging\nf-appxpackaging-iappxfile-getcontenttype.md) | Retrieves the content type of the file. |
| [IAppxFile::GetName](..\appxpackaging\nf-appxpackaging-iappxfile-getname.md) | Retrieves the name of the file, including its path relative to the package root directory. |
| [IAppxFile::GetSize](..\appxpackaging\nf-appxpackaging-iappxfile-getsize.md) | Retrieves the uncompressed size of the file. |
| [IAppxFile::GetStream](..\appxpackaging\nf-appxpackaging-iappxfile-getstream.md) | Gets a read-only stream that contains the uncompressed content of the file. |
| [IAppxFilesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxfilesenumerator-getcurrent.md) | Gets the payload file at the current position of the enumerator. |
| [IAppxFilesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxfilesenumerator-gethascurrent.md) | Determines whether there is a payload file at the current position of the enumerator. |
| [IAppxFilesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxfilesenumerator-movenext.md) | Advances the position of the enumerator to the next payload file. |
| [IAppxManifestApplication::GetAppUserModelId](..\appxpackaging\nf-appxpackaging-iappxmanifestapplication-getappusermodelid.md) | Gets the application user model identifier. |
| [IAppxManifestApplication::GetStringValue](..\appxpackaging\nf-appxpackaging-iappxmanifestapplication-getstringvalue.md) | Gets the value of a string element in the application metadata section of the manifest. |
| [IAppxManifestApplicationsEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent.md) | Gets the application at the current position of the enumerator. |
| [IAppxManifestApplicationsEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestapplicationsenumerator-gethascurrent.md) | Determines whether there is an application at the current position of the enumerator. |
| [IAppxManifestApplicationsEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext.md) | Advances the position of the enumerator to the next application. |
| [IAppxManifestDeviceCapabilitiesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestdevicecapabilitiesenumerator-getcurrent.md) | Gets the device capability at the current position of the enumerator. |
| [IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestdevicecapabilitiesenumerator-gethascurrent.md) | Determines whether there is a device capability at the current position of the enumerator. |
| [IAppxManifestDeviceCapabilitiesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxmanifestdevicecapabilitiesenumerator-movenext.md) | Advances the position of the enumerator to the next device capability. |
| [IAppxManifestMainPackageDependenciesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-getcurrent.md) | Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator. |
| [IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-gethascurrent.md) | Determines whether there is a &lt;MainPackageDependency&gt; element at the current position of the enumerator. |
| [IAppxManifestMainPackageDependenciesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-movenext.md) | Advances the position of the enumerator to the next &lt;MainPackageDependency&gt; element. |
| [IAppxManifestMainPackageDependency::GetName](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependency-getname.md) | Gets the name of the main package dependency from the AppxManifest.xml. |
| [IAppxManifestMainPackageDependency::GetPackageFamilyName](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependency-getpackagefamilyname.md) | Gets the package family name of the main package dependency from the AppxManifest.xml. |
| [IAppxManifestMainPackageDependency::GetPublisher](..\appxpackaging\nf-appxpackaging-iappxmanifestmainpackagedependency-getpublisher.md) | Gets the publisher of the main package dependency from the AppxManifest.xml. |
| [IAppxManifestOptionalPackageInfo::GetIsOptionalPackage](..\appxpackaging\nf-appxpackaging-iappxmanifestoptionalpackageinfo-getisoptionalpackage.md) | Determines whether the package is optional. |
| [IAppxManifestOptionalPackageInfo::GetMainPackageName](..\appxpackaging\nf-appxpackaging-iappxmanifestoptionalpackageinfo-getmainpackagename.md) | Gets the main package name from the optional package. |
| [IAppxManifestPackageDependenciesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-getcurrent.md) | Gets the dependency package at the current position of the enumerator. |
| [IAppxManifestPackageDependenciesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-gethascurrent.md) | Determines whether there is a package dependency at the current position of the enumerator. |
| [IAppxManifestPackageDependenciesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-movenext.md) | Advances the position of the enumerator to the next package dependency. |
| [IAppxManifestPackageDependency2::GetMaxMajorVersionTested](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependency2-getmaxmajorversiontested.md) | Returns the maximum major version number of the package that is tested to be compatible with the current package. |
| [IAppxManifestPackageDependency::GetMinVersion](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependency-getminversion.md) | Gets the minimum version of the package on which the current package has a dependency. |
| [IAppxManifestPackageDependency::GetName](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependency-getname.md) | Gets the name of the package on which the current package has a dependency. |
| [IAppxManifestPackageDependency::GetPublisher](..\appxpackaging\nf-appxpackaging-iappxmanifestpackagedependency-getpublisher.md) | Gets the name of the publisher that produced the package on which the current package depends. |
| [IAppxManifestPackageId2::GetArchitecture2 method](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid2-getarchitecture2.md) | Gets the processor architecture as defined in the manifest. |
| [IAppxManifestPackageId::ComparePublisher](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-comparepublisher.md) | Compares the specified publisher with the publisher defined in the manifest. |
| [IAppxManifestPackageId::GetArchitecture](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getarchitecture.md) | Gets the processor architecture as defined in the manifest. |
| [IAppxManifestPackageId::GetName](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getname.md) | Gets the name of the package as defined in the manifest. |
| [IAppxManifestPackageId::GetPackageFamilyName](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getpackagefamilyname.md) | Gets the package family name. |
| [IAppxManifestPackageId::GetPackageFullName](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getpackagefullname.md) | Gets the package full name. |
| [IAppxManifestPackageId::GetPublisher](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getpublisher.md) | Gets the name of the package publisher as defined in the manifest. |
| [IAppxManifestPackageId::GetResourceId](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getresourceid.md) | Gets the package resource identifier as defined in the manifest. |
| [IAppxManifestPackageId::GetVersion](..\appxpackaging\nf-appxpackaging-iappxmanifestpackageid-getversion.md) | Gets the version of the package as defined in the manifest. |
| [IAppxManifestProperties::GetBoolValue](..\appxpackaging\nf-appxpackaging-iappxmanifestproperties-getboolvalue.md) | Gets the value of the specified Boolean element in the properties section. |
| [IAppxManifestProperties::GetStringValue](..\appxpackaging\nf-appxpackaging-iappxmanifestproperties-getstringvalue.md) | Gets the value of the specified string element in the properties section. |
| [IAppxManifestReader2::GetQualifiedResources](..\appxpackaging\nf-appxpackaging-iappxmanifestreader2-getqualifiedresources.md) | Gets an enumerator that iterates through the qualified resources that are defined in the manifest. |
| [IAppxManifestReader5::GetMainPackageDependencies](..\appxpackaging\nf-appxpackaging-iappxmanifestreader5-getmainpackagedependencies.md) | Gets a main package dependencies enumerator. |
| [IAppxManifestReader6::GetIsNonQualifiedResourcePackage](..\appxpackaging\nf-appxpackaging-iappxmanifestreader6-getisnonqualifiedresourcepackage.md) | Queries whether an app package is a non-qualified resource package. |
| [IAppxManifestReader::GetApplications](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getapplications.md) | Gets an enumerator that iterates through the applications defined in the manifest. |
| [IAppxManifestReader::GetCapabilities](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getcapabilities.md) | Gets the list of capabilities requested by the package. |
| [IAppxManifestReader::GetDeviceCapabilities](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getdevicecapabilities.md) | Gets an enumerator that iterates through the device capabilities defined in the manifest. |
| [IAppxManifestReader::GetPackageDependencies](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getpackagedependencies.md) | Gets an enumerator that iterates through dependencies defined in the manifest. |
| [IAppxManifestReader::GetPackageId](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getpackageid.md) | Gets the package identifier defined in the manifest. |
| [IAppxManifestReader::GetPrerequisite](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getprerequisite.md) | Gets the specified prerequisite as defined in the package manifest. |
| [IAppxManifestReader::GetProperties](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getproperties.md) | Gets the properties of the package as defined in the manifest. |
| [IAppxManifestReader::GetResources](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getresources.md) | Gets an enumerator that iterates through the resources defined in the manifest. |
| [IAppxManifestReader::GetStream](..\appxpackaging\nf-appxpackaging-iappxmanifestreader-getstream.md) | Gets the raw XML parsed and read by the manifest reader. |
| [IAppxManifestResourcesEnumerator::GetCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestresourcesenumerator-getcurrent.md) | Gets the resource at the current position of the enumerator. |
| [IAppxManifestResourcesEnumerator::GetHasCurrent](..\appxpackaging\nf-appxpackaging-iappxmanifestresourcesenumerator-gethascurrent.md) | Determines whether there is a resource at the current position of the enumerator. |
| [IAppxManifestResourcesEnumerator::MoveNext](..\appxpackaging\nf-appxpackaging-iappxmanifestresourcesenumerator-movenext.md) | Advances the position of the enumerator to the next resource. |
| [IAppxManifestTargetDeviceFamily::GetMaxVersionTested](..\appxpackaging\nf-appxpackaging-iappxmanifesttargetdevicefamily-getmaxversiontested.md) | Gets the maximum version tested from the AppxManifest.xml. |
| [IAppxManifestTargetDeviceFamily::GetMinVersion](..\appxpackaging\nf-appxpackaging-iappxmanifesttargetdevicefamily-getminversion.md) | Gets the minimum version of the target device family from the AppxManifest.xml. |
| [IAppxManifestTargetDeviceFamily::GetName](..\appxpackaging\nf-appxpackaging-iappxmanifesttargetdevicefamily-getname.md) | Gets the name of the target device family from the AppxManifest.xml.. |
| [IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap](..\appxpackaging\nf-appxpackaging-iappxpackageeditor-createdeltapackageusingbaselineblockmap.md) | Creates a delta package from the differences in the updated package and the baseline block map. |
| [IAppxPackageEditor::CreateDeltaPackage](..\appxpackaging\nf-appxpackaging-iappxpackageeditor-createdeltapackage.md) | Creates a delta package from the differences in the updated package and the baseline package. |
| [IAppxPackageEditor::UpdateEncryptedPackage](..\appxpackaging\nf-appxpackaging-iappxpackageeditor-updateencryptedpackage.md) | Updates an encrypted app package. |
| [IAppxPackageEditor::UpdatePackageManifest](..\appxpackaging\nf-appxpackaging-iappxpackageeditor-updatepackagemanifest.md) | Updates an app package manifest. |
| [IAppxPackageEditor::UpdatePackage](..\appxpackaging\nf-appxpackaging-iappxpackageeditor-updatepackage.md) | Updates an app package. |
| [IAppxPackageReader2::GetContentGroupMap](..\appxpackaging\nf-appxpackaging-iappxpackagereader2-getcontentgroupmap.md) | Gets a content group map reader. |
| [IAppxPackageReader::GetBlockMap](..\appxpackaging\nf-appxpackaging-iappxpackagereader-getblockmap.md) | Retrieves the block map object model of the package. |
| [IAppxPackageReader::GetFootprintFile](..\appxpackaging\nf-appxpackaging-iappxpackagereader-getfootprintfile.md) | Retrieves a footprint file from the package. |
| [IAppxPackageReader::GetManifest](..\appxpackaging\nf-appxpackaging-iappxpackagereader-getmanifest.md) | Retrieves the object model of the app manifest of the package. |
| [IAppxPackageReader::GetPayloadFile](..\appxpackaging\nf-appxpackaging-iappxpackagereader-getpayloadfile.md) | Retrieves a payload file from the package. |
| [IAppxPackageReader::GetPayloadFiles](..\appxpackaging\nf-appxpackaging-iappxpackagereader-getpayloadfiles.md) | Retrieves an enumerator that iterates through the payload files in the package. |
| [IAppxPackageWriter2::Close](..\appxpackaging\nf-appxpackaging-iappxpackagewriter2-close.md) | Closes the package writer object's output stream. |
| [IAppxPackageWriter3::AddPayloadFiles](..\appxpackaging\nf-appxpackaging-iappxpackagewriter3-addpayloadfiles.md) | Adds one or more payload files to an app package. |
| [IAppxPackageWriter::AddPayloadFile](..\appxpackaging\nf-appxpackaging-iappxpackagewriter-addpayloadfile.md) | Adds a new payload file to the app package. |
| [IAppxPackageWriter::Close](..\appxpackaging\nf-appxpackaging-iappxpackagewriter-close.md) | Writes footprint files at the end of the app package, and closes the package writer object's output stream. |
| [IAppxSourceContentGroupMapReader::GetAutomaticGroups](..\appxpackaging\nf-appxpackaging-iappxsourcecontentgroupmapreader-getautomaticgroups.md) | Gets the automatic content group(s) from the source content group map. |
| [IAppxSourceContentGroupMapReader::GetRequiredGroup](..\appxpackaging\nf-appxpackaging-iappxsourcecontentgroupmapreader-getrequiredgroup.md) | Gets the required content group from the source content group map. |
